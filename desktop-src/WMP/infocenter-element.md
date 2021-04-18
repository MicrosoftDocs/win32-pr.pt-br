---
title: Elemento do InfoCenter
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento do InfoCenter
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Elemento do centro de mídia do Windows Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788158"
---
# <a name="infocenter-element"></a>Elemento do InfoCenter

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **InfoCenter** especifica a URL da página da Web que o Windows Media Player exibe no recurso de exibição do info Center de **agora em execução** quando o repositório online está ativo.

``` syntax
<InfoCenter
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

O usuário controla quando a exibição do centro de informações está ativa.

Para recuperar informações sobre o item de mídia em execução no momento, você deve inserir uma instância do controle do Windows Media Player em sua página da Web e usar o modelo de objeto do Player.

A tabela a seguir detalha os parâmetros enviados com a solicitação de URL. Outros podem estar presentes para fins de compatibilidade herdada.



| Nome         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *GeoId*      | ID da localização geográfica do Windows. A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle. |
| *locale*     | ID de localidade do Windows Media Player.                                                                                                                                     |
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

 

 





