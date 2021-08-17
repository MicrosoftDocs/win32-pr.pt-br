---
title: Elemento BuyCD
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Windows Media Player do elemento BuyCD
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0b2af0f12b06c7d5701db3fcc073d7b7c330e8798408206b64a8b9811f27d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135839"
---
# <a name="buycd-element"></a>Elemento BuyCD

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

o elemento **BuyCD** especifica as URLs para páginas da web que Windows Media Player são exibidas quando o usuário escolhe fazer uma compra.

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (obrigatório)
</dt> <dd>

A URL da página da Web que a loja online exibe para oferecer um CD ou DVD para compra no Windows Media Player.

</dd> <dt>

<span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**
</dt> <dd>

a URL da página da web que a loja online exibe para oferecer um CD ou DVD para compra na atualização do Windows XP Media Center Edition 2004.

</dd> <dt>

<span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**
</dt> <dd>

A URL da página da Web que a loja online exibe para oferecer um CD ou DVD para compra em uma janela separada do navegador. essa URL também é usada pelo Windows XP Service Pack 2 ou posterior para o recurso **comprar para música online** .

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

## <a name="remarks"></a>Comentários

quando o usuário clica em um botão ou link em Windows Media Player para comprar um CD ou DVD, o Player envia a solicitação de URL para ServiceTask1 com parâmetros anexados usando um separador de cadeia de caracteres de consulta de ponto de interrogação (?). A tabela a seguir detalha os parâmetros enviados com a solicitação de URL. Outros podem estar presentes para fins de compatibilidade herdada.



| Nome         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Álbum*      | Valor do atributo **WM/campos AlbumTitle** para o item de mídia.                                                                                                        |
| *Autor*     | Valor do atributo **WM/AlbumArtist** , se houver um, ou o valor do atributo **Author** para o item de mídia.                                         |
| *GeoId*      | ID de localização geográfica Windows. A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle. |
| *locale*     | ID de localidade Windows Media Player.                                                                                                                                     |
| *Título*      | Valor do atributo de **título** para o item de mídia.                                                                                                                |
| *UFID*       | Valor do atributo **WM/UniqueFileIdentifier** para o item de mídia.                                                                                              |
| *UserLocale* | ID de localidade Windows. A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.        |
| *version*    | Windows Media Player número de versão usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.                                                                         |



 

Windows O XP Media Center Edition 2004 fornece aos usuários uma interface do usuário projetada para ser exibida em uma distância. Você deve criar páginas da Web para que o parâmetro *MediaCenterURL* seja exibido em grandes exibições.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Documento de informações de exemplo para uma loja online tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





