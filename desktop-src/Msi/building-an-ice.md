---
description: Se não for possível localizar os avaliadores de consistência internos necessários entre as ações personalizadas de ICE existentes listadas na referência de ICE, você precisará preparar seu próprio ICE para validar seu pacote.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Criando uma ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768479"
---
# <a name="building-an-ice"></a>Criando uma ICE

Se não for possível localizar os [avaliadores de consistência internos](internal-consistency-evaluators-ices.md) necessários entre as ações personalizadas de Ice existentes listadas na [referência de Ice](ice-reference.md), você precisará preparar seu próprio Ice para validar seu pacote.

Ao criar ações personalizadas do ICE, você deve fazer o seguinte:

-   Baseie o ICEs somente em ações personalizadas de tipos listados na tabela mostrada.
-   Chame [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e poste um \_ tipo de mensagem de usuário do INSTALLMESSAGE. Ao criar suas mensagens de ICE, siga o formato da mensagem nas [diretrizes de mensagem do Ice](ice-message-guidelines.md).
-   Escreva seu ICE de modo que ele Capture quaisquer erros de API e sempre retorne o êxito do erro \_ . Isso é necessário para permitir que ações personalizadas subsequentes sejam executadas após a falha de um ICE.

As ações personalizadas do ICE são limitadas aos seguintes tipos de ação personalizadas.



| Tipo de ação personalizada                                 | Descrição               |
|----------------------------------------------------|---------------------------|
| [Tipo de ação personalizada 1](custom-action-type-1.md)   | DLL no fluxo binário      |
| [Tipo de ação personalizada 2](custom-action-type-2.md)   | EXE no fluxo binário      |
| [Tipo de ação personalizada 5](custom-action-type-5.md)   | JScript em fluxo binário  |
| [Tipo de ação personalizada 6](custom-action-type-6.md)   | VBScript em fluxo binário |
| [Tipo de ação personalizada 37](custom-action-type-37.md) | Código JScript como cadeia de caracteres    |
| [Tipo de ação personalizada 38](custom-action-type-38.md) | Código VBScript como cadeia de caracteres   |



 

Ao criar uma ação personalizada de ICE, não faça o seguinte:

-   Não assuma que o identificador para o mecanismo que o ICE recebe é uma instância de instalação do banco de dados do instalador. Se não for uma instância de instalação, determinadas propriedades não serão definidas, os diretórios de origem e de destino não serão resolvidos, e os Estados de recursos atuais não serão definidos.
-   Não confie na execução anterior, ou não na execução, de qualquer ação do instalador, ação personalizada ou outra ICE. Como uma ICE anterior pode ter criado colunas temporárias em qualquer tabela, os autores devem referenciar colunas por nome sempre que possível. ICEs deve limpar todas as colunas ou tabelas temporárias antes de sair.
-   Não presuma que os autores tenham acesso a uma imagem do diretório de origem do banco de dados.
-   Não assuma que as alterações feitas no banco de dados não persistam.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ICE de exemplo em C++](sample-ice-in-c-.md)
</dt> <dt>

[ICE de exemplo em VBScript](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



