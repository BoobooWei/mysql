# Set the access mode {#concept_jlf_hpq_wdb .concept}

RDS supports two access modes: standard mode and safe connection mode.

## Differences between standard mode and safe connection mode {#section_jf2_lqf_cfb .section}

-   **Standard mode \(recommended\)**: RDS uses [Sever Load Balancer](https://www.alibabacloud.com/help/doc-detail/27539.htm) to eliminate the impact of database engine HA switching on the application layer. This shortens the response time and increases the performance.
-   **Safe connection mode \(database proxy mode, not recommended\)**: This mode prevents 90% of disconnections, but increases the response time by 20% or more. If you are using this mode, please switch to the standard mode.

## Switch the access mode {#section_fbz_3sf_cfb .section}

**Prerequisites**

The current access mode is safe connection mode \(database proxy mode\).

**Precautions**

-   You can only switch from the database proxy mode to the standard mode.
-   If the network type of a SQL Server 2008 R2 instance is VPC, the access mode is safe connection mode and cannot be modified.
-   If the network type of a SQL Server 2008 R2 instance is classic network, the access mode is standard mode and cannot be modified.

**Method 1**

1.  Log on to the [RDS console](https://rds.console.aliyun.com/).
2.  In the upper left corner, select the region.
3.  Locate the target instance and click the instance ID.
4.  In the left-side navigation pane, click **Connection Options**.
5.  Click **Switch Access Mode**.

    **Note:** This button is available only if you have turned on the database proxy mode.


**Method 2**

1.  Log on to the [RDS console](https://rds.console.aliyun.com/).
2.  In the upper left corner, select the region.
3.  Locate the target instance and click the instance ID.
4.  In the left-side navigation pane, click **Database Proxy**.
5.  In the Database Proxy tab page, click the slider to turn off the database proxy mode.

    **Note:** This tab page is available only if you have turned on the database proxy mode.


