---
title: THEME. openDialog
description: O método openDialog abre uma caixa de diálogo de arquivo.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- THEME. openDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810676"
---
# <a name="themeopendialog"></a><span data-ttu-id="e40f3-104">THEME. openDialog</span><span class="sxs-lookup"><span data-stu-id="e40f3-104">THEME.openDialog</span></span>

<span data-ttu-id="e40f3-105">O método **openDialog** abre uma caixa de diálogo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e40f3-105">The **openDialog** method opens a file dialog box.</span></span>

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a><span data-ttu-id="e40f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e40f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e40f3-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*caixa de diálogo*</span><span class="sxs-lookup"><span data-stu-id="e40f3-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span></span>
</dt> <dd>

<span data-ttu-id="e40f3-108">Uma **cadeia de caracteres** que especifica o tipo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e40f3-108">A **String** that specifies the type of dialog box.</span></span> <span data-ttu-id="e40f3-109">Deve ser definido como "arquivo \_ aberto".</span><span class="sxs-lookup"><span data-stu-id="e40f3-109">Must be set to "FILE\_OPEN".</span></span>

</dd> <dt>

<span data-ttu-id="e40f3-110"><span id="parameters"></span><span id="PARAMETERS"></span>*parâmetro*</span><span class="sxs-lookup"><span data-stu-id="e40f3-110"><span id="parameters"></span><span id="PARAMETERS"></span>*parameters*</span></span>
</dt> <dd>

<span data-ttu-id="e40f3-111">Uma **cadeia de caracteres** que pode ser usada para obter informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="e40f3-111">A **String** that can be used for additional information.</span></span> <span data-ttu-id="e40f3-112">Deve ser definido como "arquivos de \_ mídia".</span><span class="sxs-lookup"><span data-stu-id="e40f3-112">Must be set to "FILES\_ALLMEDIA".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e40f3-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e40f3-113">Return Value</span></span>

<span data-ttu-id="e40f3-114">Esse método retorna uma **cadeia de caracteres** que contém a URL do arquivo selecionado ou "" (cadeia de caracteres vazia) se o usuário clicar em cancelar.</span><span class="sxs-lookup"><span data-stu-id="e40f3-114">This method returns a **String** containing the URL of the selected file or "" (empty string) if the user clicks cancel.</span></span>

## <a name="remarks"></a><span data-ttu-id="e40f3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e40f3-115">Remarks</span></span>

<span data-ttu-id="e40f3-116">Esse método pode ser usado para arquivos nos discos rígidos locais ou em unidades de rede.</span><span class="sxs-lookup"><span data-stu-id="e40f3-116">This method can be used for files on the local hard drives or on network drives.</span></span>

## <a name="examples"></a><span data-ttu-id="e40f3-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e40f3-117">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="e40f3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e40f3-118">Requirements</span></span>



| <span data-ttu-id="e40f3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e40f3-119">Requirement</span></span> | <span data-ttu-id="e40f3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e40f3-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e40f3-121">Versão</span><span class="sxs-lookup"><span data-stu-id="e40f3-121">Version</span></span><br/> | <span data-ttu-id="e40f3-122">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e40f3-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e40f3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e40f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40f3-124">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="e40f3-124">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





