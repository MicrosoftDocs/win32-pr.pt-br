---
description: O método GetError do objeto View retorna o erro de validação e o nome da coluna para a qual o erro ocorreu.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: Método View. GetError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749565"
---
# <a name="viewgeterror-method"></a><span data-ttu-id="ccb02-103">Método View. GetError</span><span class="sxs-lookup"><span data-stu-id="ccb02-103">View.GetError method</span></span>

<span data-ttu-id="ccb02-104">O método **GetError** do objeto [**View**](view-object.md) retorna o erro de validação e o nome da coluna para a qual o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="ccb02-104">The **GetError** method of the [**View**](view-object.md) object returns the Validation error and the column name for which the error occurred.</span></span> <span data-ttu-id="ccb02-105">Na automação, o valor retornado é uma cadeia de caracteres do formato \# \# ColumnName, em que \# \# representa um código de erro de 2 dígitos.</span><span class="sxs-lookup"><span data-stu-id="ccb02-105">In automation, the returned value is a string of the form \#\#ColumnName, where the \#\# represents a 2-digit error code.</span></span> <span data-ttu-id="ccb02-106">Ele retorna o primeiro erro na matriz de erros da exibição; as chamadas subsequentes retornam o próximo valor na matriz de erros.</span><span class="sxs-lookup"><span data-stu-id="ccb02-106">It returns the first error in the view's error array; subsequent calls return the next value in the error array.</span></span> <span data-ttu-id="ccb02-107">Quando um valor de ' 00 ' é retornado, não existem mais erros e chamadas subseqüentes simplesmente executam um loop na matriz novamente.</span><span class="sxs-lookup"><span data-stu-id="ccb02-107">Once a value of '00' is returned, no more errors exist, and subsequent calls merely loop through the array again.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb02-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccb02-108">Syntax</span></span>


```JScript
View.GetError()
```



## <a name="parameters"></a><span data-ttu-id="ccb02-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccb02-109">Parameters</span></span>

<span data-ttu-id="ccb02-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ccb02-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ccb02-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccb02-111">Return value</span></span>

<span data-ttu-id="ccb02-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ccb02-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb02-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb02-113">Requirements</span></span>



| <span data-ttu-id="ccb02-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb02-114">Requirement</span></span> | <span data-ttu-id="ccb02-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ccb02-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb02-116">Versão</span><span class="sxs-lookup"><span data-stu-id="ccb02-116">Version</span></span><br/> | <span data-ttu-id="ccb02-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ccb02-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ccb02-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ccb02-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ccb02-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccb02-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ccb02-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ccb02-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="ccb02-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccb02-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ccb02-122">IID</span><span class="sxs-lookup"><span data-stu-id="ccb02-122">IID</span></span><br/>     | <span data-ttu-id="ccb02-123">IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ccb02-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




