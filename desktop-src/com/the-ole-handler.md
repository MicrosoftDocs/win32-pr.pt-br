---
title: O manipulador OLE
description: Um manipulador OLE é uma DLL que contém vários componentes de interação usados para vincular e incorporar.
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecca46971d3ad4fdea7df6a502b2897439e03817849ad776d3e0b13a213a94f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129628"
---
# <a name="the-ole-handler"></a>O manipulador OLE

Um *manipulador OLE* é uma DLL que contém vários componentes de interação usados para vincular e incorporar. Para evitar as despesas de comunicação entre processos constantes entre um contêiner e seu servidor, o manipulador é carregado no espaço de processo do contêiner para agir em nome de um servidor como um tipo de processo substituto. O manipulador OLE gerencia solicitações de contêiner que não exigem a atenção do aplicativo de servidor, como solicitações de desenho. Quando um contêiner solicita algo que o manipulador de objetos não pode fornecer, o manipulador se comunica com o aplicativo de servidor usando o mecanismo de comunicação fora do processo COM.

Os componentes do manipulador OLE incluem partes de comunicação remoto para gerenciar a comunicação entre o manipulador e seu servidor, um cache para armazenar dados de um objeto (juntamente com informações sobre como esses dados devem ser formatados e exibidos) e um objeto de controle que coordena as atividades dos outros componentes da DLL. Além disso, se um objeto for um link, a DLL também incluirá um componente de vinculação, ou objeto vinculado *,* que mantém o controle do nome e do local da origem do link.

O OLE fornece um manipulador padrão que a maioria dos aplicativos usa para vincular e incorporar. Se o padrão não corresponder aos requisitos do servidor, você poderá substituir completamente o manipulador padrão ou usar partes da funcionalidade que ele fornece quando apropriado. No último caso, o manipulador de aplicativos é implementado como um objeto de agregação composto por um novo objeto de controle e o manipulador padrão. Manipuladores de aplicativo/padrão de combinação também são conhecidos *como manipuladores em processo.* O *manipulador de remoting* é usado para objetos que não são atribuídos a um CLSID no registro do sistema ou que não têm nenhum manipulador especificado. Tudo o que é necessário de um manipulador para esses tipos de objetos é que eles passem informações pelo limite do processo. Para criar uma nova instância do manipulador padrão, chame [**OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler). Para algumas circunstâncias especiais, chame [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper).

Quando você cria uma instância de um manipulador para uma classe, não pode usá-la para outra. Quando usado para um documento composto, o manipulador OLE implementa as estruturas de dados do lado do contêiner quando objetos de uma classe específica são acessados remotamente.

OLE definiu o manipulador padrão para clientes de servidores locais de documentos compostos. O manipulador padrão implementou várias interfaces que o servidor típico não implementou. Quando o OLE posteriormente permitia servidores em processo para documentos compostos, eles tinham que criar um auxiliar de incorporação que implementou essas interfaces extras para que os clientes pudessem trabalhar perfeitamente com eles.

Os designers de estrutura que definem e implementam um manipulador do lado do cliente devem considerar esse problema em seu design e devem fornecer um auxiliar em processo equivalente pelos mesmos motivos. Mesmo que os designers atualmente não implementem interfaces no manipulador que os servidores não expõem, talvez eles queiram definir um auxiliar agora para que possam adicioná-los no futuro. Como alternativa, é possível implementar as interfaces extras no próprio objeto de servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O manipulador de Client-Side lightweight](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




