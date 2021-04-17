---
description: Executa um teste automático do TPM e retorna o resultado.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Método SelfTest da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748392"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a><span data-ttu-id="7d104-103">Método SelfTest da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="7d104-103">SelfTest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="7d104-104">O método **SelfTest** da classe [**Win32 \_ TPM**](win32-tpm.md) executa um teste automático do TPM e retorna o resultado.</span><span class="sxs-lookup"><span data-stu-id="7d104-104">The **SelfTest** method of the [**Win32\_Tpm**](win32-tpm.md) class performs a self-test of the TPM and returns the result.</span></span>

<span data-ttu-id="7d104-105">Um teste automático do TPM é executado automaticamente quando o computador é iniciado.</span><span class="sxs-lookup"><span data-stu-id="7d104-105">A TPM self-test runs automatically when the computer starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d104-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d104-106">Syntax</span></span>


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="7d104-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d104-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d104-108">*SelfTestResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7d104-108">*SelfTestResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d104-109">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="7d104-109">Type: **uint8\[\]**</span></span>

<span data-ttu-id="7d104-110">Uma matriz de bytes que contém o resultado de autoteste.</span><span class="sxs-lookup"><span data-stu-id="7d104-110">An array of bytes that contains the self-test result.</span></span> <span data-ttu-id="7d104-111">O formato desse parâmetro é específico do fabricante.</span><span class="sxs-lookup"><span data-stu-id="7d104-111">The format of this parameter is manufacturer-specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d104-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d104-112">Return value</span></span>

<span data-ttu-id="7d104-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7d104-113">Type: **uint32**</span></span>

<span data-ttu-id="7d104-114">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="7d104-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="7d104-115">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="7d104-115">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="7d104-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7d104-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="7d104-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d104-117">Description</span></span>                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="7d104-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7d104-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="7d104-119">O método foi executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="7d104-119">The method ran successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d104-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d104-120">Remarks</span></span>

<span data-ttu-id="7d104-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7d104-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7d104-122">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="7d104-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7d104-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="7d104-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7d104-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7d104-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d104-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d104-125">Requirements</span></span>



| <span data-ttu-id="7d104-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d104-126">Requirement</span></span> | <span data-ttu-id="7d104-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7d104-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d104-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d104-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7d104-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d104-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7d104-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d104-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7d104-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7d104-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7d104-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d104-132">Namespace</span></span><br/>                | <span data-ttu-id="7d104-133">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7d104-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="7d104-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7d104-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d104-135"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="7d104-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d104-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7d104-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d104-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="7d104-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d104-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d104-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d104-139">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="7d104-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
