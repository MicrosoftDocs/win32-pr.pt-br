---
description: O método DoAction do objeto Session executa a função de ação correspondente ao nome fornecido.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Método Session. DoAction (myacquire. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782326"
---
# <a name="sessiondoaction-method"></a><span data-ttu-id="8f41d-103">Método Session. DoAction</span><span class="sxs-lookup"><span data-stu-id="8f41d-103">Session.DoAction method</span></span>

<span data-ttu-id="8f41d-104">O método **DoAction** do objeto [**Session**](session-object.md) executa a função de ação correspondente ao nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="8f41d-104">The **DoAction** method of the [**Session**](session-object.md) object executes the action function corresponding to the name supplied.</span></span> <span data-ttu-id="8f41d-105">Se um nome de ação nulo for fornecido, o mecanismo usará o valor maiúsculo da [Propriedade Action](action.md) como a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="8f41d-105">If a Null action name is supplied, the engine uses the uppercase value of the [ACTION property](action.md) as the action to perform.</span></span> <span data-ttu-id="8f41d-106">Se nenhum valor de propriedade for definido, a ação padrão será executada, atualmente definida como INSTALL.</span><span class="sxs-lookup"><span data-stu-id="8f41d-106">If no property value is defined, the default action is performed, currently defined as INSTALL.</span></span> <span data-ttu-id="8f41d-107">Esse método retorna uma enumeração de inteiros.</span><span class="sxs-lookup"><span data-stu-id="8f41d-107">This method returns an integer enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f41d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f41d-108">Syntax</span></span>


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a><span data-ttu-id="8f41d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f41d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f41d-110">*action*</span><span class="sxs-lookup"><span data-stu-id="8f41d-110">*action*</span></span> 
</dt> <dd>

<span data-ttu-id="8f41d-111">Nome da cadeia de caracteres necessária para executar.</span><span class="sxs-lookup"><span data-stu-id="8f41d-111">Required string name of the action to execute.</span></span> <span data-ttu-id="8f41d-112">Diferenciar maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8f41d-112">Case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f41d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f41d-113">Return value</span></span>

<span data-ttu-id="8f41d-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8f41d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f41d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f41d-115">Remarks</span></span>

<span data-ttu-id="8f41d-116">As ações que atualizam o sistema, como as ações [InstallFiles](installfiles-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) , não podem ser executadas chamando o método **DoAction** .</span><span class="sxs-lookup"><span data-stu-id="8f41d-116">Actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **DoAction** method.</span></span> <span data-ttu-id="8f41d-117">A exceção a essa regra é se o método **DoAction** for chamado por meio de uma ação personalizada que é agendada na [tabela InstallExecuteSequence](installexecutesequence-table.md) entre as [ações](installfinalize-action.md) [InstallInitialize](installinitialize-action.md) e InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="8f41d-117">The exception to this rule is if the **DoAction** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="8f41d-118">Ações que não atualizam o sistema, como [AppSearch](appsearch-action.md) ou [CostInitialize](costinitialize-action.md), podem ser chamadas.</span><span class="sxs-lookup"><span data-stu-id="8f41d-118">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f41d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f41d-119">Requirements</span></span>



| <span data-ttu-id="8f41d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f41d-120">Requirement</span></span> | <span data-ttu-id="8f41d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8f41d-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f41d-122">Versão</span><span class="sxs-lookup"><span data-stu-id="8f41d-122">Version</span></span><br/> | <span data-ttu-id="8f41d-123">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f41d-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8f41d-124">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8f41d-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8f41d-125">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f41d-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8f41d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f41d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8f41d-127"><dt>Metaacquire. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f41d-127"><dt>Photoacquire.h</dt></span></span> </dl>                                                                                                                                                               |
| <span data-ttu-id="8f41d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8f41d-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="8f41d-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f41d-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8f41d-130">IID</span><span class="sxs-lookup"><span data-stu-id="8f41d-130">IID</span></span><br/>     | <span data-ttu-id="8f41d-131">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8f41d-131">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




