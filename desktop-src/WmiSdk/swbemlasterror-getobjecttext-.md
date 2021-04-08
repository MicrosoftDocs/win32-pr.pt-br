---
description: O \_ método GetObjectText do objeto SWbemLastError retorna uma renderização textual do objeto em um formato formato MOF (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: Método de SWbemLastError.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921888"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a><span data-ttu-id="ea600-103">Método SWbemLastError. GetObjectText \_</span><span class="sxs-lookup"><span data-stu-id="ea600-103">SWbemLastError.GetObjectText\_ method</span></span>

<span data-ttu-id="ea600-104">O **método \_ GetObjectText** do objeto [**SWbemLastError**](swbemlasterror.md) retorna uma renderização textual do objeto em um formato [formato MOF (MOF)](managed-object-format--mof-.md) .</span><span class="sxs-lookup"><span data-stu-id="ea600-104">The **GetObjectText\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a textual rendering of the object in a [Managed Object Format (MOF)](managed-object-format--mof-.md) format.</span></span> <span data-ttu-id="ea600-105">Esse objeto MOF pode ser usado para exibir o conteúdo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ea600-105">This MOF object can be used to display an object's contents.</span></span> <span data-ttu-id="ea600-106">Observe que o texto MOF retornado não contém todas as informações sobre o objeto, mas apenas informações suficientes para o compilador MOF serem capazes de recriar o objeto original.</span><span class="sxs-lookup"><span data-stu-id="ea600-106">Notice that the MOF text that is returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="ea600-107">Por exemplo, você não encontrará nenhuma informação sobre os qualificadores propagados ou as propriedades da classe pai.</span><span class="sxs-lookup"><span data-stu-id="ea600-107">For instance, you will not find any information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="ea600-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ea600-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ea600-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea600-109">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ea600-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea600-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea600-111">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ea600-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea600-112">Esse parâmetro é reservado e deve ser 0 (zero) se especificado.</span><span class="sxs-lookup"><span data-stu-id="ea600-112">This parameter is reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea600-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea600-113">Return value</span></span>

<span data-ttu-id="ea600-114">Se for bem-sucedido, esse método retornará uma cadeia de caracteres que contém o texto de saída.</span><span class="sxs-lookup"><span data-stu-id="ea600-114">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ea600-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ea600-115">Error codes</span></span>

<span data-ttu-id="ea600-116">Após a conclusão do método **GetObjectText \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea600-116">Upon the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ea600-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ea600-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ea600-118">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="ea600-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ea600-119">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ea600-119">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ea600-120">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="ea600-120">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ea600-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ea600-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ea600-122">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="ea600-122">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea600-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea600-123">Requirements</span></span>



| <span data-ttu-id="ea600-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea600-124">Requirement</span></span> | <span data-ttu-id="ea600-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ea600-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea600-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea600-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea600-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea600-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea600-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea600-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea600-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea600-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea600-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea600-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea600-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea600-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea600-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ea600-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea600-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ea600-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ea600-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ea600-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea600-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea600-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea600-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="ea600-136">CLSID</span></span><br/>                    | <span data-ttu-id="ea600-137">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="ea600-137">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="ea600-138">IID</span><span class="sxs-lookup"><span data-stu-id="ea600-138">IID</span></span><br/>                      | <span data-ttu-id="ea600-139">ISWbemLastError de IID \_</span><span class="sxs-lookup"><span data-stu-id="ea600-139">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




