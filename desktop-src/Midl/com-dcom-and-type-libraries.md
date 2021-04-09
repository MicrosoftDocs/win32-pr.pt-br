---
title: Bibliotecas COM, DCOM e tipos
description: O COM (Component Object Model) e o Distributed Component Object Model (DCOM) usam chamadas de procedimento remoto (RPC) para permitir que objetos de componente distribuído se comuniquem entre si.
ms.assetid: 7bade397-676e-43be-82f4-b23cd768fd16
keywords:
- interfaces MIDL, COM
- interfaces MIDL, DCOM
- MIDL de interfaces, bibliotecas de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f0b21aad9f88f02d8029d478eead50f5501ecc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823731"
---
# <a name="com-dcom-and-type-libraries"></a>Bibliotecas COM, DCOM e tipos

O COM (Component Object Model) e o Distributed Component Object Model (DCOM) usam chamadas de procedimento remoto (RPC) para permitir que objetos de componente distribuído se comuniquem entre si. Portanto, uma interface COM ou DCOM define a identidade e as características externas de um objeto COM. Ele forma o meio pelo qual os clientes podem obter acesso aos métodos e dados de um objeto. Com o DCOM, esse acesso é possível independentemente de os objetos existirem no mesmo processo, processos diferentes no mesmo computador ou em máquinas diferentes. Assim como acontece com as interfaces cliente/servidor RPC, um objeto COM ou DCOM pode expor sua funcionalidade de várias maneiras diferentes e por meio de diversas interfaces.

## <a name="type-library"></a>Biblioteca de tipos

Uma biblioteca de tipos (. tlb) é um arquivo binário que armazena informações sobre as propriedades e os métodos de um objeto COM ou DCOM em um formulário que pode ser acessado por outros aplicativos em tempo de execução. Usando uma biblioteca de tipos, um aplicativo ou navegador pode determinar a quais interfaces um objeto dá suporte e invocar os métodos de interface de um objeto. Isso pode ocorrer mesmo que os aplicativos de objeto e cliente tenham sido escritos em linguagens de programação diferentes. O ambiente de tempo de execução COM/DCOM também pode usar uma biblioteca de tipos para fornecer marshaling automático entre vários apartamento, processo e entre computadores para interfaces descritas em bibliotecas de tipos.

## <a name="characteristics-of-an-interface"></a>Características de uma interface

Você define as características de uma interface em um arquivo de definição de interface (IDL) e um arquivo de configuração de aplicativo opcional (ACF):

-   O arquivo IDL especifica as características das interfaces do aplicativo na conexão, ou seja, como os dados serão transmitidos entre o cliente e o servidor ou entre objetos COM.
-   O arquivo ACF especifica características de interface, como identificadores de associação, que pertencem apenas ao ambiente operacional local. O arquivo ACF também pode especificar como realizar marshaling e transmitir uma estrutura de dados complexa em um formulário independente de máquina.

Para obter mais informações sobre arquivos IDL e ACF, consulte [os arquivos IDL e ACF](/windows/desktop/Rpc/the-idl-and-acf-files).

Os arquivos IDL e ACF são scripts escritos em linguagem IDL da Microsoft (MIDL), que é a implementação da Microsoft e a extensão da IDL (linguagem de definição de interface) uso-DCE. As extensões da Microsoft para a linguagem IDL permitem que você crie interfaces COM e bibliotecas de tipos. O compilador, Midl.exe, usa esses scripts para gerar stubs de linguagem C e arquivos de cabeçalho, bem como arquivos de biblioteca de tipos.

## <a name="the-midl-compiler"></a>O compilador MIDL

Dependendo do conteúdo do seu arquivo IDL, o compilador MIDL gerará qualquer um dos arquivos a seguir.

Um arquivo de proxy/stub do idioma C, um arquivo de identificador de interface, um arquivo de dados DLL e um arquivo de cabeçalho relacionado para uma interface COM personalizada. O compilador MIDL gera esses arquivos quando encontra o atributo Object em uma lista de atributos de interface. Para obter informações mais detalhadas sobre esses arquivos, consulte [arquivos gerados para uma interface com](files-generated-for-a-com-interface.md).

Um arquivo de biblioteca de tipos compilado (. tlb) e um arquivo de cabeçalho relacionado. O MIDL gera esses arquivos quando encontra uma instrução de [**biblioteca**](library.md) no arquivo IDL. Para obter informações gerais sobre bibliotecas de tipos, consulte [conteúdo de uma biblioteca de tipos](/previous-versions/windows/desktop/automat/contents-of-a-type-library), na referência do programador de automação.

Arquivos stub de servidor e de cliente de linguagem C/C++ e arquivo de cabeçalho relacionado para uma interface RPC. Esses arquivos são gerados quando há interfaces no arquivo IDL que não têm o atributo [**Object**](object.md) . Para obter uma visão geral dos arquivos stub e de cabeçalho, consulte [procedimento de Build geral](/windows/desktop/Rpc/general-build-procedure). Para obter informações mais detalhadas, consulte [arquivos gerados para uma interface RPC](files-generated-for-an-rpc-interface.md).

 

 