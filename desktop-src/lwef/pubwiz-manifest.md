---
title: Usando o manifesto de transferência
description: O assistente de publicação na Web e o assistente de pedido de impressão online usam o manifesto de transferência para comunicar detalhes de transferência de dados entre o computador cliente e o site do servidor.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Assistente de publicação na Web, transferir manifesto
- Assistente de ordenação de impressão online, transferir manifesto
- transferir manifesto
- manifest
- janela. external, transferir manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823758"
---
# <a name="using-the-transfer-manifest"></a>Usando o manifesto de transferência

O assistente de publicação na Web e o assistente de pedido de impressão online usam o manifesto de transferência para comunicar detalhes de transferência de dados entre o computador cliente e o site do servidor.

## <a name="the-purpose-of-the-transfer-manifest"></a>A finalidade do manifesto de transferência

O manifesto de transferência descreve os arquivos envolvidos na transferência, incluindo detalhes como a hierarquia de destino e os metadados do arquivo. O script do lado do servidor pode modificar o manifesto removendo arquivos inadequados da lista e adicionando informações sobre como e onde os arquivos devem ser transferidos.

O manifesto é exposto como a propriedade **Window. external. Property ("TransferManifest")**, um documento XML modelo de objeto do documento (dom). Para obter mais informações sobre o XML DOM, consulte a documentação do MSDN para [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).

A organização de nível superior do manifesto de transferência é a seguinte:


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



A página HTML do lado do servidor pode usar os nós no manifesto para obter determinadas informações sobre os arquivos a serem copiados e, em seguida, modificar a interface do usuário do serviço de acordo. Por exemplo, um site de impressão de fotos pode usar as informações para exibir miniaturas das imagens escolhidas, enquanto um site de armazenamento pode usar as informações para garantir que haja espaço de armazenamento suficiente disponível para esse usuário. Para obter informações completas sobre os nós e atributos de manifesto de transferência, consulte [transferir esquema de manifesto](/windows/desktop/shell/interfaces).

O esquema de manifesto de transferência é gravado como um modelo aberto para que os elementos não definidos especificamente no esquema possam aparecer no manifesto de transferência. Portanto, um site de provedor pode adicionar elementos proprietários para seu próprio uso sem perturbar a validade do manifesto. O esquema também é definido para que a ordem dos elementos não seja restrita.

> [!Note]  
> O manifesto é recriado cada vez que um novo provedor é escolhido para que o provedor tenha a chance de armazenar informações do site no manifesto.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferir esquema de manifesto](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 