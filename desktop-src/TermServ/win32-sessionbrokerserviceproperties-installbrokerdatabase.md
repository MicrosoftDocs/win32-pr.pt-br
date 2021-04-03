---
title: Método InstallBrokerDatabase da classe Win32_SessionBrokerServiceProperties
description: Instala um banco de dados do agente de conexão RD em um SQL Server central.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método InstallBrokerDatabase
- Método InstallBrokerDatabase Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Serviços de Área de Trabalho Remota, método InstallBrokerDatabase
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644324"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="2126a-106">Método InstallBrokerDatabase da classe Win32 \_ SessionBrokerServiceProperties</span><span class="sxs-lookup"><span data-stu-id="2126a-106">InstallBrokerDatabase method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="2126a-107">Instala um banco de dados do agente de conexão RD em um SQL Server central.</span><span class="sxs-lookup"><span data-stu-id="2126a-107">Installs an RD connection broker database on a central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2126a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2126a-108">Syntax</span></span>


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a><span data-ttu-id="2126a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2126a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2126a-110">*newDbFilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2126a-110">*newDbFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2126a-111">novo caminho do arquivo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2126a-111">new database file path.</span></span>

</dd> <dt>

<span data-ttu-id="2126a-112">*connStringToCentralDBMaster* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2126a-112">*connStringToCentralDBMaster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2126a-113">Cadeia de conexão para o mestre do banco de dados central.</span><span class="sxs-lookup"><span data-stu-id="2126a-113">Connection string to the central database master.</span></span>

</dd> <dt>

<span data-ttu-id="2126a-114">*centralRdcmsDbName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2126a-114">*centralRdcmsDbName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2126a-115">Nome do banco de dados central.</span><span class="sxs-lookup"><span data-stu-id="2126a-115">Name of the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2126a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2126a-116">Requirements</span></span>



| <span data-ttu-id="2126a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2126a-117">Requirement</span></span> | <span data-ttu-id="2126a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2126a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2126a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2126a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2126a-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2126a-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2126a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2126a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2126a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2126a-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="2126a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2126a-123">Namespace</span></span><br/>                | <span data-ttu-id="2126a-124">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="2126a-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="2126a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2126a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2126a-126"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2126a-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2126a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2126a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2126a-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2126a-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2126a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2126a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2126a-130">**\_SessionBrokerServiceProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="2126a-130">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





