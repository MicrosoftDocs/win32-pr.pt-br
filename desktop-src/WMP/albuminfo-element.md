---
title: Elemento AlbumInfo
description: O elemento AlbumInfo especifica a URL para a página da Web que o Windows Media Player exibe quando o usuário escolhe para exibir mais informações sobre um item de mídia específico.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Elemento AlbumInfo do Windows Media Player
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796448"
---
# <a name="albuminfo-element"></a>Elemento AlbumInfo

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **AlbumInfo** especifica a URL para a página da Web que o Windows Media Player exibe quando o usuário escolhe para exibir mais informações sobre um item de mídia específico.

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obrigatório)
</dt> <dd>

URL da página da Web exibida pelo Windows Media Player.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

## <a name="remarks"></a>Comentários

Quando o usuário clica em um botão no Windows Media Player para exibir informações adicionais sobre um item de mídia específico, o Player envia a solicitação de URL com parâmetros anexados usando um separador de cadeia de caracteres de consulta de ponto de interrogação (?). A tabela a seguir detalha os parâmetros enviados com a solicitação de URL. Outros podem estar presentes para fins de compatibilidade herdada.



| Nome         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Álbuns*      | Valor do atributo **WM/campos AlbumTitle** para o item de mídia.                                                                                                        |
| *Autor*     | Valor do atributo **WM/AlbumArtist** , se houver um, ou o valor do atributo **Author** para o item de mídia.                                         |
| *GeoId*      | ID da localização geográfica do Windows. A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle. |
| *locale*     | ID de localidade do Windows Media Player.                                                                                                                                     |
| *Título*      | Valor do atributo de **título** para o item de mídia.                                                                                                                |
| *UFID*       | Valor do atributo **WM/UniqueFileIdentifier** para o item de mídia.                                                                                              |
| *UserLocale* | IDENTIFICAÇÃO de localidade do Windows. A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.        |
| *version*    | Número de versão do Windows Media Player usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.                                                                         |



 

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

 

 





