---
title: Estados de objeto
description: Estados de objeto
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813583"
---
# <a name="object-states"></a>Estados de objeto

Um objeto composto existe em um dos três Estados: passivo, carregado ou em execução. Um estado de objeto de documento composto descreve a relação entre o objeto em seu contêiner e o aplicativo responsável por sua criação. A tabela a seguir resume esses Estados.



| Estado de objeto       | Descrição                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Passivo<br/> | O objeto de documento composto existe somente no armazenamento, seja no disco ou em um banco de dados. Nesse estado, o objeto não está disponível para exibição ou edição.<br/>                                                                                                                                                                                                                                   |
| Carregado<br/>  | As estruturas de dados do objeto criadas pelo manipulador de objetos estão na memória do contêiner. O contêiner estabeleceu comunicação com o manipulador de objetos e há dados de apresentação em cache disponíveis para renderizar o objeto. As chamadas são processadas pelo manipulador de objetos. Esse Estado, devido à baixa sobrecarga, é usado quando um usuário está simplesmente exibindo ou imprimindo um objeto.<br/> |
| Executando<br/> | Os objetos que controlam a comunicação remota foram criados e o aplicativo do servidor OLE está em execução. As interfaces do objeto são acessíveis e o contêiner pode receber a notificação de alterações. Nesse estado, um usuário final pode editar ou, de outra forma, manipular o objeto.<br/>                                                                                                                    |



 

Para mais informações, consulte os seguintes tópicos:

-   [Inserindo o estado carregado](entering-the-loaded-state.md)
-   [Entrando no estado de execução](entering-the-running-state.md)
-   [Inserindo o estado passivo](entering-the-passive-state.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> </dl>

 

 





