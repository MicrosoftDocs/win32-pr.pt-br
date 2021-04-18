---
description: O método IsPhysicalClearDisabled da classe Win32 \_ TPM indica se somente o proprietário do dispositivo pode ser capaz de limpar o dispositivo.
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Método IsPhysicalClearDisabled da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9179aae2f4902ce29e2bab98b4c9c0b793804de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761848"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="b8557-103">Método IsPhysicalClearDisabled da classe Win32 \_ TPM</span><span class="sxs-lookup"><span data-stu-id="b8557-103">IsPhysicalClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="b8557-104">O método **IsPhysicalClearDisabled** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se somente o proprietário do dispositivo pode ser capaz de limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8557-104">The **IsPhysicalClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether only the device owner may be able to clear the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8557-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8557-105">Syntax</span></span>


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="b8557-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8557-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8557-107">*IsPhysicalClearDisabled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b8557-107">*IsPhysicalClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8557-108">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b8557-108">Type: **boolean**</span></span>

<span data-ttu-id="b8557-109">Se **for true**, somente o proprietário do dispositivo poderá limpar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8557-109">If **true**, only the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8557-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8557-110">Return value</span></span>

<span data-ttu-id="b8557-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8557-111">Type: **uint32**</span></span>

<span data-ttu-id="b8557-112">Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="b8557-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="b8557-113">Os códigos de retorno comuns são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="b8557-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="b8557-114">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b8557-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="b8557-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8557-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="b8557-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b8557-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="b8557-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b8557-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8557-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8557-118">Remarks</span></span>

<span data-ttu-id="b8557-119">Esse valor é redefinido como **false** no início de cada ciclo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="b8557-119">This value is reset to **false** at the beginning of each startup cycle.</span></span>

<span data-ttu-id="b8557-120">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b8557-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b8557-121">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b8557-121">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b8557-122">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="b8557-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b8557-123">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b8557-123">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8557-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8557-124">Requirements</span></span>



| <span data-ttu-id="b8557-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8557-125">Requirement</span></span> | <span data-ttu-id="b8557-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b8557-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8557-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8557-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b8557-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8557-128">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b8557-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8557-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b8557-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8557-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b8557-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8557-131">Namespace</span></span><br/>                | <span data-ttu-id="b8557-132">\\MicrosoftTpm de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b8557-132">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="b8557-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b8557-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8557-134"><dt>\_TPM. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="b8557-134"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8557-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b8557-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8557-136"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="b8557-136"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8557-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8557-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8557-138">**TPM do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="b8557-138">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
