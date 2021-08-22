---
title: Usando o manifesto de transferência
description: O Assistente de Publicação na Web e o Assistente de Ordenação de Impressão Online usam o manifesto de transferência para comunicar detalhes da transferência de dados entre o computador cliente e o site do servidor.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Assistente de Publicação na Web, manifesto de transferência
- Assistente de Ordenação de Impressão Online, manifesto de transferência
- transferir manifesto
- manifest
- window.external,transfer manifest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d7f4ea3f9cd392f4b0bab50e1e558613fc7485d4f44a27472cd48ad898b3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555846"
---
# <a name="using-the-transfer-manifest"></a>Usando o manifesto de transferência

O Assistente de Publicação na Web e o Assistente de Ordenação de Impressão Online usam o manifesto de transferência para comunicar detalhes da transferência de dados entre o computador cliente e o site do servidor.

## <a name="the-purpose-of-the-transfer-manifest"></a>A finalidade do manifesto de transferência

O manifesto de transferência descreve os arquivos envolvidos na transferência, incluindo detalhes como a hierarquia de destino e os metadados do arquivo. O script do lado do servidor pode modificar o manifesto removendo arquivos inadequados da lista e adicionando informações sobre como e para onde os arquivos devem ser transferidos.

O manifesto é exposto como a propriedade **window.external.Property("TransferManifest")**, um documento XML Modelo de Objeto do Documento (DOM). Para obter mais informações sobre o DOM XML, consulte a documentação do MSDN [para IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).

A organização de nível superior do manifesto de transferência é a seguinte:


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



A página HTML do lado do servidor pode usar os nós no manifesto para obter determinadas informações sobre os arquivos a serem copiados e, em seguida, modificar a interface do usuário do serviço de acordo. Por exemplo, um site de impressão de fotos pode usar as informações para exibir miniaturas das imagens escolhidas, enquanto um site de armazenamento pode usar as informações para garantir que haja espaço de armazenamento suficiente disponível para esse usuário. Para obter informações completas sobre os nós e atributos do manifesto de transferência, consulte [Transferir esquema de manifesto](/windows/desktop/shell/interfaces).

O esquema de manifesto de transferência é escrito como um modelo aberto para que elementos não definidos especificamente no esquema possam aparecer no manifesto de transferência. Portanto, um site de provedor pode adicionar elementos proprietários para seu próprio uso sem atrapalhar a validade do manifesto. O esquema também é definido para que a ordem dos elementos não seja restrita.

> [!Note]  
> O manifesto é re-criado sempre que um novo provedor é escolhido para que o provedor tenha a oportunidade de armazenar informações do site no manifesto.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquema de transferência de manifesto](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 