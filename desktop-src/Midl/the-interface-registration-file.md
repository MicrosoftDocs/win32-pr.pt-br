---
title: O arquivo de registro da interface
description: O arquivo de registro de interface coleta informações que ajudam no registro de interfaces COM empacotados em um arquivo DLL ou EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- arquivo de registro de interface MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a5541a5e60b1903364236f86dcf1845a5e1ac153fc91b47bacf9f553a9a109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806174"
---
# <a name="the-interface-registration-file"></a>O arquivo de registro da interface

O arquivo de registro de interface coleta informações que ajudam no registro de interfaces COM empacotados em um arquivo DLL ou EXE. O arquivo de registro de interface é diferente de outros arquivos gerados porque ele pode coletar informações da compilação de vários arquivos IDL diferentes. Cada compilador MIDL executado para interfaces COM procura um arquivo dlldata.c existente primeiro e, se o arquivo não for encontrado, um novo arquivo dlldata.c será criado. Se um arquivo dlldata.c for encontrado, as informações sobre a IDL atual serão adicionadas (se ausentes) ou substituídas.

O arquivo de registro de interface é gerado ou atualizado com segurança em um ambiente multiprocessador porque compilações MIDL paralelas são impedidas de ser escritas no arquivo ao mesmo tempo. Como qualquer arquivo dlldata.c pode ser marcado como somente leitura pelo ambiente de build ou pelo usuário, o compilador MIDL implementa uma abordagem de tempoout para aguardar um arquivo que ele não pode abrir e emite uma mensagem de erro apropriada se o tempo-expirar.

O nome padrão para o arquivo de registro de interface gerado de um arquivo de entrada é dlldata.c. A [**opção do compilador /dlldata**](-dlldata.md) MIDL pode ser usada para substituir o nome padrão do arquivo. A substituição do nome padrão do arquivo de registro de interface é especialmente útil quando alguns arquivos IDL empacotados para um binário comum residem em diretórios diferentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando e registrando uma DLL de proxy](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 