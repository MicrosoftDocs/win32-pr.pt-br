---
description: Cria um par de chaves de endosso de 2048 bits no TPM.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Método CreateEndorsementKeyPair da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501535"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a><span data-ttu-id="86a95-103">Método CreateEndorsementKeyPair da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="86a95-103">CreateEndorsementKeyPair method of the Win32\_Tpm class</span></span>

<span data-ttu-id="86a95-104">O método **CreateEndorsementKeyPair** da classe [**Win32 \_ TPM**](win32-tpm.md) cria um par de chaves de endosso de 2048 bits no TPM.</span><span class="sxs-lookup"><span data-stu-id="86a95-104">The **CreateEndorsementKeyPair** method of the [**Win32\_Tpm**](win32-tpm.md) class creates an 2048-bit endorsement key pair on the TPM.</span></span> <span data-ttu-id="86a95-105">O par de chaves de endosso deve estar disponível para que o método [**TakeOwnership**](takeownership-win32-tpm.md) seja executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="86a95-105">The endorsement key pair must be available for the [**TakeOwnership**](takeownership-win32-tpm.md) method to run successfully.</span></span> <span data-ttu-id="86a95-106">Você pode usar o método [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) para detectar se a chave de endosso já existe no TPM.</span><span class="sxs-lookup"><span data-stu-id="86a95-106">You can use the [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) method to detect whether the endorsement key already exists on the TPM.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a95-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86a95-107">Syntax</span></span>


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a><span data-ttu-id="86a95-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86a95-108">Parameters</span></span>

<span data-ttu-id="86a95-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="86a95-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86a95-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86a95-110">Return value</span></span>

<span data-ttu-id="86a95-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86a95-111">Type: **uint32**</span></span>

<span data-ttu-id="86a95-112">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="86a95-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="86a95-113">A tabela a seguir lista alguns dos códigos de retorno comuns.</span><span class="sxs-lookup"><span data-stu-id="86a95-113">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="86a95-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="86a95-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="86a95-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="86a95-115">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="86a95-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="86a95-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="86a95-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="86a95-117">The method was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="86a95-118"><dt> **TPM \_ E \_ desabilitou \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt></span><span class="sxs-lookup"><span data-stu-id="86a95-118"><dt>**TPM\_E\_DISABLED\_CMD** </dt> <dt>2150105096 (0x80280008)</dt></span></span> </dl> | <span data-ttu-id="86a95-119">Um par de chaves de endosso já existe neste TPM.</span><span class="sxs-lookup"><span data-stu-id="86a95-119">An endorsement key pair already exists on this TPM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86a95-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="86a95-120">Remarks</span></span>

<span data-ttu-id="86a95-121">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="86a95-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="86a95-122">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="86a95-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="86a95-123">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="86a95-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="86a95-124">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="86a95-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86a95-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86a95-125">Requirements</span></span>



| <span data-ttu-id="86a95-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="86a95-126">Requirement</span></span> | <span data-ttu-id="86a95-127">Valor</span><span class="sxs-lookup"><span data-stu-id="86a95-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="86a95-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86a95-128">Minimum supported client</span></span><br/> | <span data-ttu-id="86a95-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86a95-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="86a95-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86a95-130">Minimum supported server</span></span><br/> | <span data-ttu-id="86a95-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86a95-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="86a95-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="86a95-132">Namespace</span></span><br/>                | <span data-ttu-id="86a95-133">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="86a95-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="86a95-134">MOF</span><span class="sxs-lookup"><span data-stu-id="86a95-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86a95-135"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="86a95-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="86a95-136">DLL</span><span class="sxs-lookup"><span data-stu-id="86a95-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86a95-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="86a95-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86a95-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="86a95-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a95-139">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="86a95-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
