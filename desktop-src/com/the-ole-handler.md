---
title: O manipulador OLE
description: Um manipulador OLE é uma DLL que contém vários componentes de interação usados para vinculação e inserção.
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9579f18b44a36a794ff807d9d616dd3a06dd1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005589"
---
# <a name="the-ole-handler"></a>O manipulador OLE

Um *manipulador OLE* é uma DLL que contém vários componentes de interação usados para vinculação e inserção. Para evitar a despesa de comunicação entre processos constantes entre um contêiner e seu servidor, o manipulador é carregado no espaço de processo do contêiner para atuar em nome de um servidor como um tipo de processo substituto. O manipulador OLE gerencia solicitações de contêiner que não exigem a atenção do aplicativo de servidor, como solicitações de desenho. Quando um contêiner solicita algo que o manipulador de objetos não pode fornecer, o manipulador se comunica com o aplicativo de servidor usando o mecanismo de comunicação fora do processo COM.

Os componentes do manipulador OLE incluem partes de comunicação remota para gerenciar a comunicação entre o manipulador e seu servidor, um cache para armazenar os dados de um objeto (juntamente com informações sobre como esses dados devem ser formatados e exibidos) e um objeto de controle que coordena as atividades dos outros componentes da DLL. Além disso, se um objeto for um link, a DLL também incluirá um componente de vinculação ou *objeto vinculado*, que controla o nome e o local da origem do link.

O OLE fornece um manipulador padrão que a maioria dos aplicativos usa para vinculação e inserção. Se o padrão não corresponder aos requisitos do seu servidor, você poderá substituir completamente o manipulador padrão ou usar partes da funcionalidade que ele fornece quando apropriado. No último caso, o manipulador de aplicativos é implementado como um objeto de agregação composto por um novo objeto de controle e o manipulador padrão. Os manipuladores de aplicativo/padrão de combinação também são conhecidos como *manipuladores em processo*. O *manipulador de comunicação remota* é usado para objetos que não são atribuídos a um CLSID no registro do sistema ou que não têm nenhum manipulador especificado. Tudo o que é necessário a partir de um manipulador para esses tipos de objetos é que eles passam informações entre o limite do processo. Para criar uma nova instância do manipulador padrão, chame [**OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler). Para algumas circunstâncias especiais, chame [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper).

Quando você cria uma instância de um manipulador para uma classe, não pode usá-la para outra. Quando usado para um documento composto, o manipulador OLE implementa as estruturas de dados do lado do contêiner quando os objetos de uma determinada classe são acessados remotamente.

O OLE definiu o manipulador padrão para clientes de servidores locais de documento composto. O manipulador padrão implementou várias interfaces que o servidor típico não fez. Quando o OLE permitia subseqüentemente servidores em processo para documentos compostos, eles tinham que criar um auxiliar de incorporação que implementou essas interfaces extras para que os clientes pudessem trabalhar diretamente com elas.

Os designers de estrutura que definem e implementam um manipulador do lado do cliente devem considerar esse problema em seu design e devem fornecer um auxiliar em processo equivalente pelos mesmos motivos. Mesmo que os designers não implementem interfaces no manipulador que os servidores não expõem, talvez eles queiram definir um auxiliar agora para que possam adicioná-los no futuro. Como alternativa, é possível implementar as interfaces extras no próprio objeto de servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O manipulador de Client-Side leve](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




