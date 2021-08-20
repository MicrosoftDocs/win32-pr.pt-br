---
title: Elemento Image (SDK do WMP)
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento Image (SDK do WMP)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Elemento Image Windows Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9815844833c8068fb89589368f29b15787ad8fb18a21c9f9c6867d202e3095a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862636"
---
# <a name="image-element-wmp-sdk"></a>Elemento Image (SDK do WMP)

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O **elemento Image** especifica as imagens Windows Media Player exibidas ao usuário para representar o armazenamento online.

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (necessário para armazenamentos de tipo 1, ignorado para o tipo 2)
</dt> <dd>

URL para o logotipo que Windows Media Player exibido na caixa de diálogo EULA (Contrato de Licença do Usuário Final). Essa deve ser uma imagem PNG de 80 x 80 pixels.

</dd> <dt>

<span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (opcional)
</dt> <dd>

URL para a imagem Windows Media Player exibida no menu serviços. Essa imagem deve ter 15 x 15 pixels.

</dd> <dt>

<span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (opcional)
</dt> <dd>

Para uma loja online do tipo 1, essa é a URL para a imagem Windows Media Player exibida na **guia Lojas** Online. Por Windows Media Player 11, essa imagem deve ter 45 pixels de largura por 13 pixels de altura. Por Windows Media Player 12, essa imagem deve ter 45 pixels de largura por 30 pixels de altura. Para dar suporte às versões 11 e 12 do Windows Media Player, você deve fornecer dois documentos ServiceInfo.xml separados, cada um deles aponta para a imagem de tamanho apropriado para ServiceLargeURL.

Para uma loja online do tipo 2, essa é a URL para a imagem Windows Media Player exibida ao lado da guia **Lojas Online** ou ao lado dos botões do painel de tarefas. Essa imagem deve ter 30 x 30 pixels.

</dd> <dt>

<span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (opcional)
</dt> <dd>

URL para o logotipo exibido junto com a descrição de marketing especificada no elemento **Description.** Se não for fornecido, ele ficará em branco. (Todos os tipos, opcional) Essa deve ser uma imagem PNG com 45 pixels de largura e 13 pixels de altura.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

## <a name="remarks"></a>Comentários

Os formatos de imagem com suporte .gif, .jpg, .bmp e .png (que é o formato recomendado). O uso da transparência da Web tem suporte e é recomendado. Não há suporte para arquivos GIF animados.

Se você não fornecer um valor para **MenuURL,** Windows Media Player não exibirá nenhum gráfico no menu da loja online.

Você pode fornecer uma imagem animada para ServiceLargeURL. No Windows Media Player 10 ou 11, a imagem é animada. No Windows Media Player 12, somente o primeiro quadro da imagem é exibido. Para fornecer uma imagem animada, crie um único arquivo de imagem que contenha quadros sucessivos de sua animação. Por exemplo, para uma imagem com 30 pixels de largura e 30 pixels de altura, você pode fornecer 20 imagens sucessivas lado a lado em uma imagem com 600 pixels de largura e 30 pixels de altura. Windows Media Player animaria automaticamente essa imagem mostrando as 20 imagens individuais uma após a outra. Essa animação ocorre apenas uma vez quando a loja online é aberta; ele não se repete.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Documento ServiceInfo de exemplo para uma loja online do tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de exemplo para uma loja online do tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





