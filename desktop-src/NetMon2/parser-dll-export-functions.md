---
description: As funções, listadas na tabela a seguir, são pontos de entrada para DLLs do analisador. As funções são os pontos de entrada para chamadas do sistema operacional e Monitor de Rede.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Funções de exportação de DLL do analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370594"
---
# <a name="parser-dll-export-functions"></a>Funções de exportação de DLL do analisador

As funções, listadas na tabela a seguir, são pontos de entrada para DLLs do analisador. As funções são os pontos de entrada para chamadas do sistema operacional e Monitor de Rede.



| Função                                           | Descrição                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Analisador DllMain](dllmain-parser.md)               | Indica para a DLL do analisador que está carregada ou descarregada. O sistema operacional chama a função de **analisador DllMain** quando um processo carrega ou descarrega a dll. |
| [Anexarproperties](attachproperties.md)           | Notifica o analisador para anexar qualquer propriedade existente em um quadro.                                                                                            |
| [Cancelar registro](deregister.md)                       | Notifica o analisador para limpar.                                                                                                                               |
| [Formatproperties](formatproperties.md)           | Notifica o analisador para pegar todas as instâncias de propriedade no e criar o membro **szPropertyText** de cada estrutura **PROPERTYINST** .                       |
| [RecognizeFrame](recognizeframe.md)               | Determina se o analisador pode interpretar os dados de quadro não processados com o protocolo especificado.                                                            |
| [Registrar analisador](register-parser.md)             | Determina as informações básicas sobre o analisador dentro da DLL. Monitor de Rede chama a função de **analisador de registro** .                                          |
| [ParserAutoInstallInfo](parserautoinstallinfo.md) | Instala automaticamente um analisador.                                                                                                                               |



 

Monitor de Rede fornece estruturas e funções auxiliares que o analisador pode chamar.



| Para saber mais sobre                          | Consulte                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| Funções auxiliares que podem ser chamadas por especialistas e analisadores. | [Funções comuns de expert e parser](expert-and-parser-common-functions.md) |
| Funções auxiliares que somente analisadores podem chamar.        | [Funções do analisador](parser-functions.md)                                     |
| Estruturas usadas por funções de analisador.               | [Estruturas do analisador](parser-structures.md)                                   |



 

 

 



