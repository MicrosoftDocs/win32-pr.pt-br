---
description: Este tópico descreve como seu aplicativo pode especificar qual URL o computador tablet Ferramenta de Captura deve obter ao capturar seu aplicativo.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Ferramenta de Captura suporte no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2c24901524500df97461f3b3acf88d9a51f73cc24134955c1df866a457a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966765"
---
# <a name="snipping-tool-support-in-windows-vista"></a>Ferramenta de Captura suporte no Windows Vista

Este tópico descreve como seu aplicativo pode especificar qual URL o computador tablet Ferramenta de Captura deve obter ao capturar seu aplicativo.

## <a name="specifying-the-url-via-registry-key"></a>Especificando a URL por meio da chave do Registro

Ferramenta de Captura permite que os usuários capturem um snip (captura de tela) de qualquer objeto na tela e, em seguida, anotam, salvam ou compartilham a imagem. Quando os dados são salvos em formato HTML ou quando são enviados a um cliente de email que dá suporte a HTML em linha, o Ferramenta de Captura pode adicionar uma URL ao snip se o aplicativo fornece informações sobre como obter a URL.

Ferramenta de Captura obtém a URL por meio de objetos de acessibilidade. Os aplicativos devem especificar as informações necessárias nas seguintes chaves do Registro:

HKLM \\ Software Microsoft Windows \\ \\ \\ TabletPC Ferramenta de Captura \\ \\ LinkPrints,

E deve criar uma sub-chave cujo nome é o mesmo que a classe de janela da qual o link deve ser obtido. O nome da classe de janela deve ser a janela mais alta do aplicativo.

HKLM \\ Software Microsoft Windows \\ \\ \\ TabletPC Ferramenta de Captura \\ \\ LinkPrints\\<Window Class Name>

### <a name="window-class-key-details"></a>Detalhes da chave da classe window

Na chave de classe da janela, os valores apropriados devem ser definidos para indicar Ferramenta de Captura deve detectar o objeto de acessibilidade correto.



| VALOR                        | TYPE                  | Máscara            | INFORMAÇÕES ARMAZENADAS                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Mask<br/>              | REG \_ DWORD<br/> |                 | Indica quais dos campos a seguir verificar<br/> |
| Nome<br/>              | REG \_ SZ<br/>    | 0x02<br/> | Nome da acessibilidade<br/>                               |
| Descrição<br/>       | REG \_ SZ<br/>    | 0x04<br/> | Descrição da acessibilidade<br/>                        |
| Função<br/>              | REG \_ DWORD<br/> | 0x08<br/> | Função de acessibilidade<br/>                               |
| ParentName<br/>        | REG \_ SZ<br/>    | 0x10<br/> | Nome de acessibilidade do pai<br/>                     |
| ParentValue<br/>       | REG \_ SZ<br/>    | 0x20<br/> | Valor de acessibilidade do pai<br/>                    |
| ParentRole<br/>        | REG \_ DWORD<br/> | 0x40<br/> | Função de acessibilidade do pai<br/>                     |
| ParentDescription<br/> | REG \_ SZ<br/>    | 0x80<br/> | Descrição de acessibilidade do pai<br/>              |



 

Além disso, se o valor de bit de máscara 0x1 estiver definido, a URL deverá ser retirada do nome de acessibilidade; caso contrário, a URL deverá ser retirada do valor de acessibilidade.

Se o aplicativo usar cadeias de caracteres localizadas para os valores de REG SZ acima, a cadeia de caracteres deverá ser fornecida como uma cadeia de caracteres indireta \_ usando o seguinte formato:

@filenameRecurso

A cadeia de caracteres é extraída do arquivo chamado , usando o valor do recurso como um localizador. Se o valor do recurso for zero ou maior, o número se tornará o índice da cadeia de caracteres no arquivo binário. Se o número for negativo, ele se tornará um ID (identificador de recurso).

> [!Note]  
> As constantes de função podem ser encontradas em oleacc.h no SDK do Windows. Os valores do Registro descritos são específicos Windows Vista.

 

 

 




