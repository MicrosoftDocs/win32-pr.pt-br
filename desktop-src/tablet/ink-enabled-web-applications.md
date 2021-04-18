---
description: O exemplo de blog de tinta demonstra várias técnicas úteis que podem ser usadas em aplicativos Web habilitados para tinta.
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Ink-Enabled aplicativos Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b14e368c1d2e97e35afa6d72a0fe082f304c5fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815587"
---
# <a name="ink-enabled-web-applications"></a>Ink-Enabled aplicativos Web

O exemplo de [blog de tinta](ink-blog-web-sample.md) demonstra várias técnicas úteis que podem ser usadas em aplicativos Web habilitados para tinta. Isso inclui: testar se o computador cliente pode dar suporte a controles habilitados para tinta, enviar dados de tinta para um servidor e exibir dados de tinta em uma página da Web.

## <a name="testing-ink-enablement"></a>Testando a habilitação de tinta

Pode ser útil testar se o computador cliente pode exibir controles habilitados para tinta. Isso permite que você tenha thewebpageshow um controle se o cliente for um Tablet PC ou outro, se não estiver. Uma maneira de testar isso é tentar criar um objeto, como um [InkOverlay](/previous-versions/ms833057(v=msdn.10)), que só pode ser criado em um computador com o Windows Vista, o sistema operacional Windows XP Tablet PC Edition ou o SDK (Software Development Kit) do Windows XP Tablet PC Edition instalado. Se você criar o objeto dentro de um bloco try/catch e capturar todas as exceções que são lançadas (geralmente, um [FileNotFoundException](/previous-versions/windows/) é lançado para indicar que o assembly com esse controle não pode ser encontrado), você pode detectar se o computador cliente pode dar suporte a controles habilitados para tinta. No exemplo, esse código pode ser encontrado no construtor da `InkArea` classe.

## <a name="submitting-ink-data"></a>Enviando dados de tinta

Uma maneira simples de enviar dados é pegar os dados do seu controle habilitado para tinta, transferi-los para um formato oculto e, em seguida, enviar o formulário. A tinta pode ser serializada usando o método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) e, em seguida, convertida em uma cadeia de caracteres. No exemplo, o formulário oculto é definido em addblog. aspx, e a serialização de tinta é manipulada em `InkArea.SerializeInkData` , onde a tinta é serializada em uma imagem GIF. (Observe que ele poderia ser serializado da mesma forma em outros formatos, como o ISF (Ink serializado Format).)

## <a name="displaying-ink-data"></a>Exibindo dados de tinta

No exemplo, addblog. aspx. cs tem um método chamado `Page_Load` que recupera os dados que são postados no servidor e salva-os em arquivos. Em seguida, ele gera páginas da Web no servidor que contém marcas img que fazem referência aos arquivos com as imagens GIF. Agora você só precisa navegar até essas páginas para ver as imagens da tinta. (Observe que, se você tivesse serializado a tinta com um formato diferente, como o ISF (Ink serializado Format), precisaria converter a tinta em uma imagem no servidor para exibi-la em clientes que não são Tablets.)

Os clientes do Tablet PC podem carregar a tinta de volta em um controle habilitado para tinta e permitir que o usuário edite a tinta usando ISF. Isso é verdadeiro mesmo para tinta salva usando o valor **GIF** da enumeração [PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) , porque os dados ISF estão contidos nos metadados gif.

 

 
