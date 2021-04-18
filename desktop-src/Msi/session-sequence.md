---
description: O método Sequence do objeto Session abre uma consulta na tabela especificada, ordenando as ações pelos números na coluna sequence.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Método Session. Sequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748967"
---
# <a name="sessionsequence-method"></a><span data-ttu-id="f118a-103">Método Session. Sequence</span><span class="sxs-lookup"><span data-stu-id="f118a-103">Session.Sequence method</span></span>

<span data-ttu-id="f118a-104">O método **Sequence** do objeto [**Session**](session-object.md) abre uma consulta na tabela especificada, ordenando as ações pelos números na coluna sequence.</span><span class="sxs-lookup"><span data-stu-id="f118a-104">The **Sequence** method of the [**Session**](session-object.md) object opens a query on the specified table, ordering the actions by the numbers in the Sequence column.</span></span> <span data-ttu-id="f118a-105">Para cada linha buscada, o método [**DoAction**](session-doaction.md) é chamado, desde que qualquer expressão de condição fornecida não seja avaliada como false.</span><span class="sxs-lookup"><span data-stu-id="f118a-105">For each row fetched, the [**DoAction**](session-doaction.md) method is called, provided that any supplied condition expression does not evaluate to False.</span></span> <span data-ttu-id="f118a-106">Retorna um msiDoActionStatusEnum de enumeração, conforme descrito no método [**DoAction**](session-doaction.md) .</span><span class="sxs-lookup"><span data-stu-id="f118a-106">Returns an enumeration msiDoActionStatusEnum, as described in the [**DoAction**](session-doaction.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f118a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f118a-107">Syntax</span></span>


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a><span data-ttu-id="f118a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f118a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f118a-109">*table*</span><span class="sxs-lookup"><span data-stu-id="f118a-109">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="f118a-110">Nome de cadeia de caracteres necessário da tabela a ser usada para sequenciamento.</span><span class="sxs-lookup"><span data-stu-id="f118a-110">Required string name of the table to use for sequencing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f118a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f118a-111">Return value</span></span>

<span data-ttu-id="f118a-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f118a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f118a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f118a-113">Remarks</span></span>

<span data-ttu-id="f118a-114">Esse método normalmente é chamado internamente por ações de nível superior.</span><span class="sxs-lookup"><span data-stu-id="f118a-114">This method is normally called internally by top-level actions.</span></span>

<span data-ttu-id="f118a-115">Uma sequência de ação que contém ações que atualizam o sistema, como as ações [InstallFiles](installfiles-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) , não pode ser executada chamando o método **Sequence** .</span><span class="sxs-lookup"><span data-stu-id="f118a-115">An action sequence containing actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **Sequence** method.</span></span> <span data-ttu-id="f118a-116">A exceção a essa regra é se o método **Sequence** for chamado por meio de uma ação personalizada agendada na [tabela InstallExecuteSequence](installexecutesequence-table.md) entre as ações [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="f118a-116">The exception to this rule is if the **Sequence** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="f118a-117">Ações que não atualizam o sistema, como [AppSearch](appsearch-action.md) ou [CostInitialize](costinitialize-action.md), podem ser chamadas.</span><span class="sxs-lookup"><span data-stu-id="f118a-117">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="f118a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f118a-118">Requirements</span></span>



| <span data-ttu-id="f118a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f118a-119">Requirement</span></span> | <span data-ttu-id="f118a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f118a-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f118a-121">Versão</span><span class="sxs-lookup"><span data-stu-id="f118a-121">Version</span></span><br/> | <span data-ttu-id="f118a-122">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f118a-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f118a-123">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f118a-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f118a-124">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f118a-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f118a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f118a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="f118a-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f118a-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f118a-127">IID</span><span class="sxs-lookup"><span data-stu-id="f118a-127">IID</span></span><br/>     | <span data-ttu-id="f118a-128">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f118a-128">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




