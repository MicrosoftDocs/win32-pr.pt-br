---
title: Elemento InfoCenter
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento InfoCenter
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Elemento InfoCenter Windows Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1d89e7a35d0d9daacd87d3ac840f0ee87fa7c82b317afd54c9283344e204f8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576255"
---
# <a name="infocenter-element"></a>Elemento InfoCenter

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **elemento InfoCenter** especifica a URL da página da Web Windows Media Player exibida no  recurso Exibição do Info Center de Agora Em Reprodução quando a loja online está ativa.

``` syntax
<InfoCenter
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

O usuário controla quando o Info Center View está ativo.

Para recuperar informações sobre o item de mídia em reprodução no momento, você deve inserir uma instância do controle Windows Media Player em sua página da Web e usar o modelo de objeto Player.

A tabela a seguir detalha os parâmetros enviados com a solicitação de URL. Outros podem estar presentes para fins de compatibilidade herdado.



| Name         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows ID de localização geográfica. A ID de local é especificada pelo usuário na **área** Local das configurações De Opções Regionais e de Idioma Painel de Controle. |
| *locale*     | Windows Media Player ID da localidade.                                                                                                                                     |
| *userlocale* | Windows ID de localidade. A localidade é especificada pelo usuário na área Padrões e **Formatos** das configurações Opções Regionais e de Idioma Painel de Controle.        |
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

 

 





