---
title: Método GenerateReportEx da classe Win32_TSLicenseReport
description: Gera um relatório de uso de licença atual para licenças por usuário e por dispositivo.
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GenerateReportEx
- Método GenerateReportEx Serviços de Área de Trabalho Remota, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Serviços de Área de Trabalho Remota, método GenerateReportEx
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893e6e29d1e4716560b0f0f6b41e6109c89e2f5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369315"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="0e47c-106">Método GenerateReportEx da classe Win32 \_ TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="0e47c-106">GenerateReportEx method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="0e47c-107">Gera um relatório de uso de licença atual para licenças por usuário e por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e47c-107">Generates a current license usage report for both Per User and Per Device licenses.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e47c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e47c-108">Syntax</span></span>


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="0e47c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e47c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e47c-110">*Nome do arquivo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0e47c-110">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e47c-111">O nome do arquivo do relatório gerado.</span><span class="sxs-lookup"><span data-stu-id="0e47c-111">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e47c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e47c-112">Return value</span></span>

<span data-ttu-id="0e47c-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="0e47c-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0e47c-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0e47c-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0e47c-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0e47c-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e47c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e47c-116">Remarks</span></span>

<span data-ttu-id="0e47c-117">Esse é um método estático.</span><span class="sxs-lookup"><span data-stu-id="0e47c-117">This is a static method.</span></span>

<span data-ttu-id="0e47c-118">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="0e47c-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0e47c-119">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0e47c-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0e47c-120">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0e47c-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0e47c-121">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="0e47c-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0e47c-122">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0e47c-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e47c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e47c-123">Requirements</span></span>



| <span data-ttu-id="0e47c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e47c-124">Requirement</span></span> | <span data-ttu-id="0e47c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0e47c-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e47c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e47c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e47c-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0e47c-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="0e47c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e47c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e47c-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e47c-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="0e47c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e47c-130">Namespace</span></span><br/>                | <span data-ttu-id="0e47c-131">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="0e47c-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="0e47c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0e47c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e47c-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e47c-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e47c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0e47c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e47c-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e47c-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e47c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e47c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e47c-137">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="0e47c-137">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

