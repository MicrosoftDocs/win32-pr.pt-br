---
title: Propriedade SystemMonitor SqlDsnName
description: Recupera ou define o nome da fonte de dados ODBC (DSN).
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Propriedade SqlDsnName SysMon
- Propriedade SqlDsnName SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, Propriedade SqlDsnName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369200"
---
# <a name="systemmonitorsqldsnname-property"></a><span data-ttu-id="fba8b-106">Propriedade SystemMonitor:: SqlDsnName</span><span class="sxs-lookup"><span data-stu-id="fba8b-106">SystemMonitor::SqlDsnName property</span></span>

<span data-ttu-id="fba8b-107">Recupera ou define o nome da fonte de dados ODBC (DSN).</span><span class="sxs-lookup"><span data-stu-id="fba8b-107">Retrieves or sets the ODBC data source name (DSN).</span></span>

## <a name="syntax"></a><span data-ttu-id="fba8b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fba8b-108">Syntax</span></span>


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a><span data-ttu-id="fba8b-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fba8b-109">Property value</span></span>

<span data-ttu-id="fba8b-110">O nome da fonte de dados ODBC que aponta para um banco de dado que contém as tabelas Perfmon corretas.</span><span class="sxs-lookup"><span data-stu-id="fba8b-110">ODBC data source name that points to a database that contains the correct Perfmon tables.</span></span> <span data-ttu-id="fba8b-111">O formato é SQL: DSN.</span><span class="sxs-lookup"><span data-stu-id="fba8b-111">The format is SQL:DSN.</span></span>

## <a name="remarks"></a><span data-ttu-id="fba8b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fba8b-112">Remarks</span></span>

<span data-ttu-id="fba8b-113">Você deve usar o snap-in do MMC Perfmon. msc para gerar o arquivo de log do SQL.</span><span class="sxs-lookup"><span data-stu-id="fba8b-113">You must use the Perfmon.msc MMC snap-in to generate the SQL log file.</span></span> <span data-ttu-id="fba8b-114">Os logs de contador estão localizados em **logs e alertas de desempenho**.</span><span class="sxs-lookup"><span data-stu-id="fba8b-114">The counter logs are located under **Performance Logs and Alerts**.</span></span> <span data-ttu-id="fba8b-115">Para especificar um log SQL, clique com o botão direito do mouse no arquivo de log que você criou e selecione **Propriedades** no menu.</span><span class="sxs-lookup"><span data-stu-id="fba8b-115">To specify an SQL log, right-click the log file you created and select **Properties** from the menu.</span></span> <span data-ttu-id="fba8b-116">Na página de propriedades **arquivos de log** , selecione **banco de dados SQL** na caixa de listagem suspensa **tipo de arquivo de log** .</span><span class="sxs-lookup"><span data-stu-id="fba8b-116">On the **Log Files** property page, select **SQL Database** from the **Log file type** drop-down list box.</span></span>

<span data-ttu-id="fba8b-117">**Antes do Windows Vista:** Você não poderá modificar essa propriedade se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for definido como [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="fba8b-117">**Prior to Windows Vista:** You cannot modify this property if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="fba8b-118">Você deve primeiro especificar o nome e, em seguida, definir **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonSqlLog**.</span><span class="sxs-lookup"><span data-stu-id="fba8b-118">You must first specify the name and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonSqlLog**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba8b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fba8b-119">Requirements</span></span>



| <span data-ttu-id="fba8b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba8b-120">Requirement</span></span> | <span data-ttu-id="fba8b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fba8b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fba8b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fba8b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fba8b-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fba8b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fba8b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fba8b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fba8b-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fba8b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fba8b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fba8b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba8b-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="fba8b-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba8b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fba8b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba8b-129">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="fba8b-129">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="fba8b-130">**SystemMonitor.SqlLogSetName**</span><span class="sxs-lookup"><span data-stu-id="fba8b-130">**SystemMonitor.SqlLogSetName**</span></span>](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





