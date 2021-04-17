---
title: Método Error. Item
description: O método item recupera um objeto ErrorItem da fila de erros.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe de erro
- Classe de erro Windows Media Player, método de item
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762076"
---
# <a name="erroritem-method"></a><span data-ttu-id="d4ab7-106">Método Error. Item</span><span class="sxs-lookup"><span data-stu-id="d4ab7-106">Error.item method</span></span>

<span data-ttu-id="d4ab7-107">O método **Item** recupera um objeto **ErrorItem** da fila de erros.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-107">The **item** method retrieves an **ErrorItem** object from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ab7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4ab7-108">Syntax</span></span>


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="d4ab7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4ab7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ab7-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d4ab7-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ab7-111">**Número** (**longo**) que contém o índice do objeto **ErrorItem** a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-111">**Number** (**long**) containing the index of the **ErrorItem** object to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ab7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4ab7-112">Return value</span></span>

<span data-ttu-id="d4ab7-113">Esse método retorna um objeto **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="d4ab7-113">This method returns an **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4ab7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4ab7-114">Remarks</span></span>

<span data-ttu-id="d4ab7-115">O Windows Media Player pode gerar vários erros em resposta a uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-115">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="d4ab7-116">Esse método permite a recuperação de um erro específico na fila usando um número de índice.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-116">This method allows the retrieval of a specific error in the queue by using an index number.</span></span> <span data-ttu-id="d4ab7-117">Os números de índice para a fila de erros começam com zero.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-117">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="d4ab7-118">Você deve definir *as configurações*. **enableErrorDialogs** como false se você optar por exibir mensagens de erro personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-118">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="d4ab7-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d4ab7-119">Examples</span></span>

<span data-ttu-id="d4ab7-120">O exemplo de JScript a seguir usa o *erro*. objeto de **Item** em um manipulador de eventos para alertar o usuário para o erro mais recente.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-120">The following JScript example uses the *Error*.**item** object in an event handler to alert the user to the most recent error.</span></span> <span data-ttu-id="d4ab7-121">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d4ab7-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a><span data-ttu-id="d4ab7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4ab7-122">Requirements</span></span>



| <span data-ttu-id="d4ab7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4ab7-123">Requirement</span></span> | <span data-ttu-id="d4ab7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d4ab7-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ab7-125">Versão</span><span class="sxs-lookup"><span data-stu-id="d4ab7-125">Version</span></span><br/> | <span data-ttu-id="d4ab7-126">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d4ab7-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d4ab7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d4ab7-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4ab7-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4ab7-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ab7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4ab7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ab7-130">**Objeto Error**</span><span class="sxs-lookup"><span data-stu-id="d4ab7-130">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="d4ab7-131">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="d4ab7-131">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





