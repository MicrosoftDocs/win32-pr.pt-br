---
title: Negociação de Media-Type
description: Muitos protocolos de Internet de camada de aplicativo são baseados na troca de mensagens em um formato simples e flexível chamado MIME (Multipurpose Internet Mail Extensions).
ms.assetid: 7a2c9d8f-639a-4865-a62b-63330175f5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb145fa3a76da6574172ddd24888f3b5da7ad85e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366771"
---
# <a name="media-type-negotiation"></a>Negociação de Media-Type

Muitos protocolos de Internet de camada de aplicativo são baseados na troca de mensagens em um formato simples e flexível chamado MIME (Multipurpose Internet Mail Extensions). Embora o MIME tenha sido originado como um padrão para a troca de mensagens de email eletrônica, ele é usado hoje por uma ampla variedade de aplicativos para especificar formatos de dados mutuamente compreendidos como MIME, ou tipos de mídia. O processo é chamado de *negociação de tipo de mídia*.

Os tipos de mídia são cadeias de caracteres simples que denotam um tipo e subtipo (como "texto/simples" ou "texto/HTML"). Eles são usados para rotular dados ou qualificar uma solicitação. Um navegador da Web, por exemplo, como parte de um HTTP Request-for-data ou Request-for-info, especifica que ele está solicitando os tipos de mídia "image/gif" ou "image/jpeg", ao qual um servidor Web responde retornando o tipo de mídia apropriado e, se a chamada foi uma solicitação-para-dados, os dados em si no formato solicitado

A negociação de tipo de mídia geralmente é semelhante a como os aplicativos de área de trabalho existentes negociam com a área de transferência do sistema para determinar qual formato de dados colar quando um usuário escolhe Editar/colar ou consultas para formatos ao receber um ponteiro do [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) durante uma operação de arrastar e soltar. A diferença sutil na negociação do tipo de mídia HTTP é que o cliente não sabe antecipadamente quais formatos o servidor está disponível. Portanto, o cliente especifica os tipos de mídia aos quais ele dá suporte, em ordem de maior fidelidade, e o servidor responde com o melhor formato disponível.

Os monikers de URL dão suporte à negociação de tipo de mídia como uma maneira para os clientes e servidores da Internet concordarem em formatos a serem usados ao baixar dados em operações [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) . Para dar suporte à negociação de tipo de mídia, um cliente implementa a interface [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) e chama a função [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)) para registrá-la com o contexto de associação. O enumerador de formato lista os formatos que o cliente pode aceitar. Um moniker de URL converte esses formatos em tipos de mídia ao ligar a URLs HTTP.

Os tipos de mídia possíveis solicitados pelo cliente são representados para os monikers de URL por meio de estruturas [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) disponíveis no enumerador [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) registrado pelo chamador no contexto de associação: cada **FORMATETC** especifica um formato de área de transferência que identifica o tipo de mídia. Por exemplo, o fragmento de código a seguir especifica que o tipo de mídia é PostScript.

``` syntax
FORMATETC fmtetc;
fmtetc.cfFormat = RegisterClipboardFormat(CF_MIME_POSTSCRIPT);
. . .
```

Um cliente pode definir o formato da área de transferência para o tipo de mídia especial CF \_ NULL para indicar que o tipo de mídia padrão do recurso apontado pela URL deve ser recuperado. Esse formato é geralmente o último em que o cliente está interessado. Quando nenhum enumerador é registrado com o contexto de ligação, um moniker de URL funciona como se um enumerador contendo um único [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) com **cfFormat**= CF \_ NULL estiver disponível, baixando automaticamente o tipo de mídia padrão.

Seja qual for o tipo de mídia a ser usado, o cliente é notificado sobre a escolha por meio do argumento *pFormatetc* em seu método [**IBindStatusCallback:: OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . O retorno de chamada ocorre no contexto da chamada do cliente para [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage).

> [!Note]  
> Se o conteúdo recebido for de um tipo de mídia não reconhecido, o cliente chamará automaticamente [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) para registrar o novo tipo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Identificadores de URL](url-monikers.md)
</dt> </dl>

 

 