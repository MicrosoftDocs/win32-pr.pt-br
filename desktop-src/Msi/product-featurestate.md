---
description: A propriedade Featurestate é o estado de instalação do recurso para a instância deste produto. Essa propriedade chama MsiQueryFeatureStateEx, com o ProductCode, userid e o contexto do objeto. A ID do recurso é fornecida como um parâmetro.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Método Product. Featurestate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750222"
---
# <a name="productfeaturestate-method"></a><span data-ttu-id="fddc5-104">Método Product. Featurestate</span><span class="sxs-lookup"><span data-stu-id="fddc5-104">Product.FeatureState method</span></span>

<span data-ttu-id="fddc5-105">A propriedade **featurestate** é o estado de instalação do recurso para a instância deste produto.</span><span class="sxs-lookup"><span data-stu-id="fddc5-105">The **FeatureState** property is the installation state of the feature for the instance of this product.</span></span>

<span data-ttu-id="fddc5-106">Essa propriedade chama [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), com o *ProductCode*, *userid* e o *contexto* do objeto.</span><span class="sxs-lookup"><span data-stu-id="fddc5-106">This property calls [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), with the *ProductCode*, *UserSid* and *Context* of the object.</span></span> <span data-ttu-id="fddc5-107">A ID do recurso é fornecida como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fddc5-107">The feature Id is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fddc5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fddc5-108">Syntax</span></span>


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a><span data-ttu-id="fddc5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fddc5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fddc5-110">*Recurso de funcionalidade*</span><span class="sxs-lookup"><span data-stu-id="fddc5-110">*FeatureId*</span></span> 
</dt> <dd>

<span data-ttu-id="fddc5-111">ID do recurso que aparece na coluna recurso da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="fddc5-111">Feature Id appearing in the Feature column of the [Feature Table](feature-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fddc5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fddc5-112">Return value</span></span>

<span data-ttu-id="fddc5-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fddc5-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fddc5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fddc5-114">Remarks</span></span>

<span data-ttu-id="fddc5-115">Se a chamada for bem sucedido, a propriedade conterá o valor como um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="fddc5-115">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="fddc5-116">Estado</span><span class="sxs-lookup"><span data-stu-id="fddc5-116">State</span></span>                    | <span data-ttu-id="fddc5-117">Significado</span><span class="sxs-lookup"><span data-stu-id="fddc5-117">Meaning</span></span>                                      |
|--------------------------|----------------------------------------------|
| <span data-ttu-id="fddc5-118">INSTALLstate \_ anunciado</span><span class="sxs-lookup"><span data-stu-id="fddc5-118">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="fddc5-119">Este recurso é anunciado.</span><span class="sxs-lookup"><span data-stu-id="fddc5-119">This feature is advertised.</span></span>                  |
| <span data-ttu-id="fddc5-120">INSTALAR \_ local</span><span class="sxs-lookup"><span data-stu-id="fddc5-120">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="fddc5-121">O recurso é instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="fddc5-121">The feature is installed locally.</span></span>            |
| <span data-ttu-id="fddc5-122">origem de INSTALLstate \_</span><span class="sxs-lookup"><span data-stu-id="fddc5-122">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="fddc5-123">O recurso é instalado para ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="fddc5-123">The feature is installed to run from source.</span></span> |



 

<span data-ttu-id="fddc5-124">Se a chamada falhar, a propriedade conterá um código de erro de [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span><span class="sxs-lookup"><span data-stu-id="fddc5-124">If the call fails, the property contains an error code from [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span></span>



| <span data-ttu-id="fddc5-125">Erro</span><span class="sxs-lookup"><span data-stu-id="fddc5-125">Error</span></span>                     | <span data-ttu-id="fddc5-126">Significado</span><span class="sxs-lookup"><span data-stu-id="fddc5-126">Meaning</span></span>                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fddc5-127">ERRO de \_ acesso \_ negado</span><span class="sxs-lookup"><span data-stu-id="fddc5-127">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="fddc5-128">O processo de chamada deve ter privilégios administrativos para obter informações de um produto instalado para um usuário que não seja o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="fddc5-128">The calling process must have administrative privileges to get information for a product installed for a user other than the current user.</span></span> |
| <span data-ttu-id="fddc5-129">ERRO \_ de \_ configuração incorreta</span><span class="sxs-lookup"><span data-stu-id="fddc5-129">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="fddc5-130">Os dados de configuração estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="fddc5-130">The configuration data is corrupt.</span></span>                                                                                                         |
| <span data-ttu-id="fddc5-131">\_parâmetro inválido de erro \_</span><span class="sxs-lookup"><span data-stu-id="fddc5-131">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="fddc5-132">Um parâmetro inválido foi passado para a função.</span><span class="sxs-lookup"><span data-stu-id="fddc5-132">An invalid parameter was passed to the function.</span></span>                                                                                           |
| <span data-ttu-id="fddc5-133">êxito do erro \_</span><span class="sxs-lookup"><span data-stu-id="fddc5-133">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="fddc5-134">A função foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="fddc5-134">The function completed successfully.</span></span>                                                                                                       |
| <span data-ttu-id="fddc5-135">ERRO \_ desconhecido \_ recurso</span><span class="sxs-lookup"><span data-stu-id="fddc5-135">ERROR\_UNKNOWN\_FEATURE</span></span>   | <span data-ttu-id="fddc5-136">A ID do recurso não identifica um recurso conhecido.</span><span class="sxs-lookup"><span data-stu-id="fddc5-136">The feature ID does not identify a known feature.</span></span>                                                                                          |
| <span data-ttu-id="fddc5-137">ERRO \_ de \_ produto desconhecido</span><span class="sxs-lookup"><span data-stu-id="fddc5-137">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="fddc5-138">O código do produto não identifica um produto conhecido.</span><span class="sxs-lookup"><span data-stu-id="fddc5-138">The product code does not identify a known product.</span></span>                                                                                        |
| <span data-ttu-id="fddc5-139">\_falha na função de erro \_</span><span class="sxs-lookup"><span data-stu-id="fddc5-139">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="fddc5-140">Uma falha interna inesperada.</span><span class="sxs-lookup"><span data-stu-id="fddc5-140">An unexpected internal failure.</span></span>                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="fddc5-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fddc5-141">Requirements</span></span>



| <span data-ttu-id="fddc5-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="fddc5-142">Requirement</span></span> | <span data-ttu-id="fddc5-143">Valor</span><span class="sxs-lookup"><span data-stu-id="fddc5-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fddc5-144">Versão</span><span class="sxs-lookup"><span data-stu-id="fddc5-144">Version</span></span><br/> | <span data-ttu-id="fddc5-145">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fddc5-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fddc5-146">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fddc5-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fddc5-147">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fddc5-147">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="fddc5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fddc5-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="fddc5-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fddc5-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="fddc5-150">IID</span><span class="sxs-lookup"><span data-stu-id="fddc5-150">IID</span></span><br/>     | <span data-ttu-id="fddc5-151">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fddc5-151">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="fddc5-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="fddc5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fddc5-153">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="fddc5-153">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="fddc5-154">**MsiQueryFeatureStateEx**</span><span class="sxs-lookup"><span data-stu-id="fddc5-154">**MsiQueryFeatureStateEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[<span data-ttu-id="fddc5-155">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="fddc5-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




