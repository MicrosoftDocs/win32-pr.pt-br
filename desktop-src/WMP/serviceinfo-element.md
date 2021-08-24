---
title: Elemento ServiceInfo
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento ServiceInfo é o elemento principal para o ServiceInfo.xml documento.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Elemento ServiceInfo Windows Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b3be774d019555daa75b78edf6a7ed76351e7523712313365dd6c80bfee7cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763636"
---
# <a name="serviceinfo-element"></a>Elemento ServiceInfo

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **elemento ServiceInfo** é o elemento principal para o ServiceInfo.xml documento.

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a>Atributos



| Termo                                                                                                                                             | Descrição                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Versão** (opcional)<br/> | Versão do arquivo ServiceInfo.xml dados. A versão 1.00 tem suporte para Windows Media Player.<br/>                                                                                                                                                            |
| <span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Chave** (obrigatório)<br/>                 | A cadeia de caracteres de chave de serviço que identifica exclusivamente o armazenamento online.<br/>                                                                                                                                                                                   |
| <span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**<br/>                 | Indica se a loja online é um armazenamento do tipo 1. Um valor "true" indica que o armazenamento é um armazenamento do tipo 1. Um valor de "false" indica que o armazenamento não é um armazenamento do tipo 1; ou seja, é um armazenamento de tipo 2. O valor padrão é "falso".<br/> |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai | Nenhum                                                                                                                                                                               |
| Elementos filho  | **AlbumInfo,** **BuyCD,** **Color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **InfoCenter**, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |



 

## <a name="remarks"></a>Comentários

A tabela a seguir detalha os parâmetros enviados com a solicitação de URL. Outros podem estar presentes para fins de compatibilidade herdado. A solicitação também incluirá todos os parâmetros especificados usando o parâmetro de linha de comando ServiceExtra da Windows Media Player configuração.



| Nome         | Valor                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows ID de localização geográfica. A ID de local é especificada pelo usuário na **área** Local das configurações De Opções Regionais e de Idioma Painel de Controle. |
| *locale*     | Windows Media Player ID da localidade.                                                                                                                                     |
| *userlocale* | Windows ID da localidade. A localidade é especificada pelo usuário na área Padrões e **Formatos** das configurações De opções Regionais e de Idioma Painel de Controle.        |
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

 

 





