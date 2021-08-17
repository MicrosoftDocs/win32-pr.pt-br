---
description: O exemplo de Blog do Ink demonstra várias técnicas úteis que podem ser usadas em aplicativos Web habilitados para tinta.
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Ink-Enabled Aplicativos Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8097bd55c34abbcb4469d74642e9dbc9a5f29e3b0b7110a76543fd40f5b1ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043487"
---
# <a name="ink-enabled-web-applications"></a>Ink-Enabled Aplicativos Web

O [exemplo de Blog](ink-blog-web-sample.md) do Ink demonstra várias técnicas úteis que podem ser usadas em aplicativos Web habilitados para tinta. Isso inclui: testar se o computador cliente pode dar suporte a controles habilitados para tinta, enviar dados de tinta para um servidor e exibir dados de tinta em uma página da Web.

## <a name="testing-ink-enablement"></a>Testando a habilitação de tinta

Pode ser útil testar se o computador cliente pode exibir controles habilitados para tinta. Isso permite que você tenha awebpageshow um controle se o cliente for um tablet pc ou outro, se não for. Uma maneira de testar isso é tentar criar um objeto como [um InkOverlay](/previous-versions/ms833057(v=msdn.10)), que só pode ser criado em um computador que tenha o sistema operacional do Windows Vista, do Windows XP Tablet PC Edition ou do SDK (Software Development Kit) do Windows XP Tablet Pc Edition instalado. Se você criar o objeto dentro de um bloco try/catch e capturar todas as exceções que são lançadas (geralmente, [uma FileNotFoundException](/previous-versions/windows/) é lançada para indicar que o assembly com esse controle não pode ser encontrado), você pode detectar se o computador cliente pode dar suporte a controles habilitados para tinta. No exemplo, esse código pode ser encontrado no construtor da `InkArea` classe .

## <a name="submitting-ink-data"></a>Enviando dados de tinta

Uma maneira simples de enviar dados é pegar os dados do controle habilitado para tinta, transferi-los para um formulário oculto e enviar o formulário. A tinta pode ser serializada usando o [método Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) e convertida em uma Cadeia de Caracteres. No exemplo, o formulário oculto é definido em AddBlog.aspx e a serialização de tinta é tratada em , em que a tinta é serializada em uma `InkArea.SerializeInkData` imagem GIF. (Observe que ele também pode ser serializado de forma semelhante em outros formatos, como FORMATO serializado de tinta (ISF).)

## <a name="displaying-ink-data"></a>Exibindo dados de tinta

No exemplo, AddBlog.aspx.cs tem um método chamado que recupera os dados postados no servidor e os salva `Page_Load` em arquivos. Em seguida, ele gera páginas da Web no servidor que contém marcas img que referenciam os arquivos com as imagens GIF. Agora você só precisa navegar até essas páginas para ver imagens da tinta. (Observe que, se você tivesse serializado a tinta com um formato diferente, como formato ISF (ISF), você precisaria converter a tinta em uma imagem no servidor para exibi-la em clientes que não são tablets.)

Os clientes de tablet pc podem carregar a tinta de volta em um controle habilitado para tinta e permitir que o usuário edite a tinta usando ISF. Isso é verdadeiro até mesmo para tinta salva usando o valor **Gif** da enumeração [PersistenceFormat,](/previous-versions/ms827245(v=msdn.10)) porque os dados ISF estão contidos nos metadados GIF.

 

 
