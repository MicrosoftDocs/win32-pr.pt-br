---
title: Elemento DownloadStatus (msfeeds. h)
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento DownloadStatus (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Elemento DownloadStatus do Windows Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758222"
---
# <a name="downloadstatus-element"></a>Elemento DownloadStatus

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **DownloadStatus** especifica uma URL que o Windows Media Player exibe como um link para permitir que os usuários exibam o status de download.

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="URL"></span><span id="url"></span>URL
</dt> <dd>

URL para a página da Web que a loja online exibe para mostrar o status de download para o usuário.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

## <a name="remarks"></a>Comentários

O Windows Media Player exibe uma mensagem para os usuários quando um download está em andamento. Se os serviços ativos atuais definirem uma URL de status de download, o usuário poderá clicar no texto da mensagem. Quando o usuário clica na mensagem, o Player navega até a URL especificada pelo elemento **DownloadStatus** para que o repositório ativo atual possa fornecer detalhes sobre os downloads em andamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/>                                          |
| parâmetro<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Documento de informações de exemplo para uma loja online tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





