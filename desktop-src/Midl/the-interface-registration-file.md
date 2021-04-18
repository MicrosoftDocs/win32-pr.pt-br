---
title: O arquivo de registro da interface
description: O arquivo de registro de interface coleta informações que ajudam no registro de interfaces COM empacotadas em um arquivo DLL ou EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- arquivo de registro da interface MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758971"
---
# <a name="the-interface-registration-file"></a>O arquivo de registro da interface

O arquivo de registro de interface coleta informações que ajudam no registro de interfaces COM empacotadas em um arquivo DLL ou EXE. O arquivo de registro da interface é diferente de outros arquivos gerados porque ele pode coletar informações da compilação de vários arquivos IDL diferentes. Cada compilador MIDL executado para interfaces COM procura um arquivo dlldata. c existente primeiro e, se o arquivo não for encontrado, um novo arquivo dlldata. c será criado. Se um arquivo dlldata. c for encontrado, as informações sobre o IDL atual serão adicionadas (se ausentes) ou substituídas.

O arquivo de registro da interface é gerado com segurança ou atualizado em um ambiente multiprocessador, pois compilações de MIDL paralelas são impedidas de gravar no arquivo ao mesmo tempo. Como qualquer arquivo dlldata. c pode ser marcado como somente leitura pelo ambiente de compilação ou pelo usuário, o compilador MIDL implementa uma abordagem de tempo limite para aguardar um arquivo que ele não pode abrir e emite uma mensagem de erro apropriada se o tempo limite expirar.

O nome padrão para o arquivo de registro da interface gerado a partir de um arquivo de entrada é dlldata. c. A opção de compilador [**/dlldata nomedearquivo**](-dlldata.md) MIDL pode ser usada para substituir o nome padrão do arquivo. Substituir o nome padrão do arquivo de registro da interface é especialmente útil quando alguns arquivos IDL empacotados em um binário comum residem em diretórios diferentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando e registrando uma DLL de proxy](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 