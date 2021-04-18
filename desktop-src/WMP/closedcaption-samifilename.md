---
title: ClosedCaption.SAMIFileName
description: A propriedade SAMIFileName especifica ou recupera o nome do arquivo que contém as informações necessárias para Legendagem oculta.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption. SAMIFileName Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810574"
---
# <a name="closedcaptionsamifilename"></a><span data-ttu-id="d91a5-104">ClosedCaption.SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="d91a5-104">ClosedCaption.SAMIFileName</span></span>

<span data-ttu-id="d91a5-105">A propriedade **SAMIFileName** especifica ou recupera o nome do arquivo que contém as informações necessárias para Legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="d91a5-105">The **SAMIFileName** property specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a><span data-ttu-id="d91a5-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d91a5-106">Possible Values</span></span>

<span data-ttu-id="d91a5-107">Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d91a5-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d91a5-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d91a5-108">Remarks</span></span>

<span data-ttu-id="d91a5-109">O arquivo de intercâmbio de mídia acessível (SAMI) sincronizado deve usar uma extensão de nome de arquivo. SMI ou. Sami.</span><span class="sxs-lookup"><span data-stu-id="d91a5-109">The Synchronized Accessible Media Interchange (SAMI) file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="d91a5-110">Se você não especificar um valor para **SAMIFileName**, essa propriedade recuperará uma cadeia de caracteres que contém o nome do arquivo ou a URL associada ao item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="d91a5-110">If you don't specify a value for **SAMIFileName**, this property retrieves a string containing the file name or URL associated with the current media item.</span></span> <span data-ttu-id="d91a5-111">Essa associação pode ocorrer quando um arquivo SAMI é especificado usando o parâmetro de URL *Sami* , ou automaticamente quando o arquivo Sami tem o mesmo nome que o nome do arquivo de mídia digital (exceto para a extensão de nome de arquivo).</span><span class="sxs-lookup"><span data-stu-id="d91a5-111">This association can occur when a SAMI file is specified using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file name (except for the file name extension).</span></span> <span data-ttu-id="d91a5-112">Se não houver nenhum arquivo SAMI associado à mídia atual, essa propriedade recuperará uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="d91a5-112">If there is no SAMI file associated with the current media, this property retrieves an empty string ("").</span></span>

<span data-ttu-id="d91a5-113">Depois de especificar um valor para **SAMIFileName**, esse valor persiste até que você especifique um novo valor (ou até que um novo item de mídia seja aberto usando o parâmetro de URL *Sami* ).</span><span class="sxs-lookup"><span data-stu-id="d91a5-113">Once you specify a value for **SAMIFileName**, that value persists until you specify a new value (or until a new media item is opened using the *sami* URL parameter).</span></span> <span data-ttu-id="d91a5-114">Portanto, você deve especificar um novo valor para essa propriedade antes de reproduzir cada novo item de mídia.</span><span class="sxs-lookup"><span data-stu-id="d91a5-114">Therefore, you must specify a new value for this property before you play each new media item.</span></span> <span data-ttu-id="d91a5-115">Dessa forma, o novo valor de **SAMIFileName** entrará em vigor quando o próximo item de mídia for aberto (ou quando o *Player*.**fechar** é chamado).</span><span class="sxs-lookup"><span data-stu-id="d91a5-115">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when *Player*.**close** is called).</span></span> <span data-ttu-id="d91a5-116">A especificação de um novo valor para **SAMIFileName** não tem nenhum efeito para a mídia atual.</span><span class="sxs-lookup"><span data-stu-id="d91a5-116">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="d91a5-117">Para fazer com que o Windows Media Player volte a usar o arquivo SAMI associado a um item de mídia específico, especifique um valor para **SAMIFileName** igual a uma cadeia de caracteres vazia ("") antes de reproduzir o próximo item de mídia.</span><span class="sxs-lookup"><span data-stu-id="d91a5-117">To cause Windows Media Player to return to using the SAMI file associated with a particular media item, specify a value for **SAMIFileName** equal to an empty string ("") before you play the next media item.</span></span>

<span data-ttu-id="d91a5-118">**Windows Media Player 10 Mobile:** Essa propriedade é somente leitura e sempre retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="d91a5-118">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="d91a5-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d91a5-119">Examples</span></span>

<span data-ttu-id="d91a5-120">Os três exemplos de JScript a seguir usam *ClosedCaption*. **SAMIFileName** para especificar o nome de um arquivo de texto de legenda oculta.</span><span class="sxs-lookup"><span data-stu-id="d91a5-120">The following three JScript examples use *ClosedCaption*.**SAMIFileName** to specify the name of a closed caption text file.</span></span> <span data-ttu-id="d91a5-121">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d91a5-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a><span data-ttu-id="d91a5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d91a5-122">Requirements</span></span>



| <span data-ttu-id="d91a5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d91a5-123">Requirement</span></span> | <span data-ttu-id="d91a5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d91a5-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d91a5-125">Versão</span><span class="sxs-lookup"><span data-stu-id="d91a5-125">Version</span></span><br/> | <span data-ttu-id="d91a5-126">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d91a5-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d91a5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d91a5-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="d91a5-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d91a5-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d91a5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d91a5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d91a5-130">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="d91a5-130">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="d91a5-131">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="d91a5-131">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="d91a5-132">**Player. fechar**</span><span class="sxs-lookup"><span data-stu-id="d91a5-132">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





