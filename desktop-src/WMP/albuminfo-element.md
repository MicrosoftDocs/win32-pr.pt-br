---
title: Elemento AlbumInfo
description: O elemento AlbumInfo especifica a URL da página da Web que Windows Media Player é exibida quando o usuário opta por exibir mais informações sobre um item de mídia específico.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Elemento AlbumInfo Windows Media Player
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a5f8fab7da8f61ce6ee5451ebcef4dc33517aae2396f0817fac19222713db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055374"
---
# <a name="albuminfo-element"></a>Elemento AlbumInfo

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **elemento AlbumInfo** especifica a URL da página da Web Windows Media Player exibida quando o usuário opta por exibir mais informações sobre um item de mídia específico.

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obrigatório)
</dt> <dd>

URL para a página da Web Windows Media Player exibida.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

## <a name="remarks"></a>Comentários

Quando o usuário clica em um botão no Windows Media Player para exibir informações adicionais sobre um item de mídia específico, o Player envia a solicitação de URL com parâmetros anexados usando um separador de cadeia de caracteres de consulta de ponto de interrogação (?). A tabela a seguir detalha os parâmetros enviados com a solicitação de URL. Outros podem estar presentes para fins de compatibilidade herdado.



| Nome         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Álbum*      | Valor do atributo **WM/AlbumTitle** para o item de mídia.                                                                                                        |
| *Artista*     | Valor do **atributo WM/AlbumArtist,** se houver ou o valor do atributo **Author** para o item de mídia.                                         |
| *Geoid*      | Windows ID de localização geográfica. A ID de local é especificada pelo usuário na **área** Local das configurações De Opções Regionais e de Idioma Painel de Controle. |
| *locale*     | Windows Media Player ID da localidade.                                                                                                                                     |
| *Título*      | Valor do atributo **Title** para o item de mídia.                                                                                                                |
| *UFID*       | Valor do **atributo WM/UniqueFileIdentifier** para o item de mídia.                                                                                              |
| *userlocale* | Windows ID da localidade. A localidade é especificada pelo usuário na área Padrões e **Formatos** das configurações Opções Regionais e de Idioma Painel de Controle.        |
| *version*    | Windows Media Player número de versão usando o seguinte formato: 10.0.x.xxxx ou 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Documento ServiceInfo de exemplo para uma loja online do tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de exemplo para uma loja online do tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





