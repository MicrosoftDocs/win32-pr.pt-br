---
description: Exemplos de controles dos pais
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Exemplos de controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781599"
---
# <a name="parental-controls-samples"></a>Exemplos de controles dos pais

O código de exemplo para controles dos pais está disponível em caminho <installation directory> \\ Windows \\ <version number> \\ Samples \\ Security \\ ParentalControls. Os exemplos são os seguintes:

## <a name="utilities"></a>Utilitários

Funcionalidade auxiliar para gerenciamento COM básico, operações de cadeia de caracteres de SID e funcionalidade de leitura e gravação do WMI. Todos os outros exemplos dependem deste projeto, a menos que especificado de outra forma.

## <a name="complianceapi"></a>ComplianceAPI

Aplicativo de console orientado por linha de comando demonstrando como usar a API de conformidade para recuperar um subconjunto de chaves de configurações para um usuário.

## <a name="complianceapp"></a>ComplianceApp

Aplicativo de console simples que demonstra o uso da API de conformidade para verificar o registro em log necessário e restrições específicas. Se as restrições de tempo estiverem habilitadas, o aplicativo também aguardará os eventos de logout iminentes.

## <a name="uiextensibility"></a>UIExtensibility

Aplicativo de console orientado por linha de comando demonstrando o uso das APIs do WMI e do esquema WPC para listar, consultar, adicionar, modificar e excluir entradas do link de extensibilidade da interface do usuário.

Exemplo de linha de comando para exemplo:

"D: \\ WPC \\ Samples \\ Security \\ ParentalControls \\ UIExtensibility \\ debug \\ UIExtensibility" Add/g: {FD59BB7F-54AB-11DB-9666-00E08161165F}/c: 0/N: D:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-101/S: D:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-103/I: D:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-104/D: d:/WPC/Samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-106/e: c: \\ Windows \\Notepad.exe

em que UiExtRC é uma DLL de recurso simples com recursos de cadeia de caracteres para a ID 101 e 103 e 24x24 pixel 32-bit com Bitmaps alfa para recursos 104 e 106.

## <a name="webextensibility"></a>Webextensibility

Aplicativo de console orientado por linha de comando demonstrando como usar as APIs WMI e o esquema WPC para listar, adicionar e excluir entradas de isenção de URL ou aplicativo HTTP e para definir e redefinir uma substituição de filtro de conteúdo da Web com as propriedades Filterid e FilterName.

O acesso ao aplicativo HTTP somente leitura e às listas de isenção de URL não é mostrado, mas o código para ler as listas seria o mesmo para o caso de leitura/gravação, exceto para a modificação do parâmetro WMI.

 

 



