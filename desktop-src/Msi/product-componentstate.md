---
description: A propriedade Componentstate é o estado de instalação do componente para a instância deste produto. Essa propriedade chama MsiQueryComponentState, com o ProductCode, userid e o contexto do objeto.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Método Product. Componentstate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748140"
---
# <a name="productcomponentstate-method"></a><span data-ttu-id="62a35-103">Método Product. Componentstate</span><span class="sxs-lookup"><span data-stu-id="62a35-103">Product.ComponentState method</span></span>

<span data-ttu-id="62a35-104">A propriedade **componentstate** é o estado de instalação do componente para a instância deste produto.</span><span class="sxs-lookup"><span data-stu-id="62a35-104">The **ComponentState** property is the installation state of the component for the instance of this product.</span></span>

<span data-ttu-id="62a35-105">Essa propriedade chama [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), com o ProductCode, userid e o contexto do objeto.</span><span class="sxs-lookup"><span data-stu-id="62a35-105">This property calls [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), with the ProductCode, UserSid, and Context of the object.</span></span> <span data-ttu-id="62a35-106">O GUID de ID de componente é fornecido como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="62a35-106">The component Id GUID is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a35-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62a35-107">Syntax</span></span>


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a><span data-ttu-id="62a35-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62a35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a35-109">*ID*</span><span class="sxs-lookup"><span data-stu-id="62a35-109">*ID*</span></span> 
</dt> <dd>

<span data-ttu-id="62a35-110">GUID de código de componente do componente como encontrado na coluna ComponentID da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="62a35-110">Component code GUID of the component as found in the ComponentID column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a35-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62a35-111">Return value</span></span>

<span data-ttu-id="62a35-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="62a35-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62a35-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="62a35-113">Remarks</span></span>

<span data-ttu-id="62a35-114">Se a chamada for bem sucedido, a propriedade conterá o valor como um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="62a35-114">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="62a35-115">Estado</span><span class="sxs-lookup"><span data-stu-id="62a35-115">State</span></span>                | <span data-ttu-id="62a35-116">Significado</span><span class="sxs-lookup"><span data-stu-id="62a35-116">Meaning</span></span>                                            |
|----------------------|----------------------------------------------------|
| <span data-ttu-id="62a35-117">INSTALAR \_ local</span><span class="sxs-lookup"><span data-stu-id="62a35-117">INSTALLSTATE\_LOCAL</span></span>  | <span data-ttu-id="62a35-118">O componente é instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="62a35-118">The component is installed locally.</span></span>                |
| <span data-ttu-id="62a35-119">origem de INSTALLstate \_</span><span class="sxs-lookup"><span data-stu-id="62a35-119">INSTALLSTATE\_SOURCE</span></span> | <span data-ttu-id="62a35-120">O componente é instalado para ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="62a35-120">The component is installed to run from the source.</span></span> |



 

<span data-ttu-id="62a35-121">Se a chamada falhar, a propriedade conterá um código de erro de [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span><span class="sxs-lookup"><span data-stu-id="62a35-121">If the call fails, the property contains an error code from [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span></span>



| <span data-ttu-id="62a35-122">Erro</span><span class="sxs-lookup"><span data-stu-id="62a35-122">Error</span></span>                     | <span data-ttu-id="62a35-123">Significado</span><span class="sxs-lookup"><span data-stu-id="62a35-123">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a35-124">ERRO de \_ acesso \_ negado</span><span class="sxs-lookup"><span data-stu-id="62a35-124">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="62a35-125">O processo de chamada deve ter privilégios administrativos para obter informações para um usuário que não seja o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="62a35-125">The calling process must have administrative privileges to get information for a user other than the current user.</span></span> |
| <span data-ttu-id="62a35-126">ERRO \_ de \_ configuração incorreta</span><span class="sxs-lookup"><span data-stu-id="62a35-126">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="62a35-127">Os dados de configuração estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="62a35-127">The configuration data is corrupt.</span></span>                                                                                 |
| <span data-ttu-id="62a35-128">\_parâmetro inválido de erro \_</span><span class="sxs-lookup"><span data-stu-id="62a35-128">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="62a35-129">Um parâmetro inválido foi passado para a função.</span><span class="sxs-lookup"><span data-stu-id="62a35-129">An invalid parameter was passed to the function.</span></span>                                                                   |
| <span data-ttu-id="62a35-130">êxito do erro \_</span><span class="sxs-lookup"><span data-stu-id="62a35-130">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="62a35-131">A função foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="62a35-131">The function completed successfully.</span></span>                                                                               |
| <span data-ttu-id="62a35-132">ERRO \_ de \_ componente desconhecido</span><span class="sxs-lookup"><span data-stu-id="62a35-132">ERROR\_UNKNOWN\_COMPONENT</span></span> | <span data-ttu-id="62a35-133">A ID do componente não identifica um componente conhecido.</span><span class="sxs-lookup"><span data-stu-id="62a35-133">The component ID does not identify a known component.</span></span>                                                              |
| <span data-ttu-id="62a35-134">ERRO \_ de \_ produto desconhecido</span><span class="sxs-lookup"><span data-stu-id="62a35-134">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="62a35-135">O código do produto não identifica um produto conhecido.</span><span class="sxs-lookup"><span data-stu-id="62a35-135">The product code does not identify a known product.</span></span>                                                                |
| <span data-ttu-id="62a35-136">\_falha na função de erro \_</span><span class="sxs-lookup"><span data-stu-id="62a35-136">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="62a35-137">Uma falha interna inesperada.</span><span class="sxs-lookup"><span data-stu-id="62a35-137">An unexpected internal failure.</span></span>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="62a35-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62a35-138">Requirements</span></span>



| <span data-ttu-id="62a35-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a35-139">Requirement</span></span> | <span data-ttu-id="62a35-140">Valor</span><span class="sxs-lookup"><span data-stu-id="62a35-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a35-141">Versão</span><span class="sxs-lookup"><span data-stu-id="62a35-141">Version</span></span><br/> | <span data-ttu-id="62a35-142">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="62a35-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62a35-143">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="62a35-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62a35-144">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="62a35-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="62a35-145">DLL</span><span class="sxs-lookup"><span data-stu-id="62a35-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="62a35-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a35-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="62a35-147">IID</span><span class="sxs-lookup"><span data-stu-id="62a35-147">IID</span></span><br/>     | <span data-ttu-id="62a35-148">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="62a35-148">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="62a35-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="62a35-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a35-150">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="62a35-150">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="62a35-151">**MsiQueryComponentState**</span><span class="sxs-lookup"><span data-stu-id="62a35-151">**MsiQueryComponentState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[<span data-ttu-id="62a35-152">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="62a35-152">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




