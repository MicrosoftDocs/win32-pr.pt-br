---
title: Compilação MIDL
description: Compilação MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a94f94122aeeb1f2900c3adec7e567c794f31ee22259f657dfe5e95f3f688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047944"
---
# <a name="midl-compilation"></a>Compilação MIDL

Dado um arquivo IDL, como [Example2.idl,](anatomy-of-an-idl-file.md)que define uma ou mais interfaces COM e uma biblioteca de tipos, o compilador MIDL (Midl.exe) gera os arquivos descritos na tabela a seguir como a saída padrão.



| Nome de arquivo                 | Descrição                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Example2.h<br/>    | O arquivo de header, que contém definições de tipo e declarações de função para todas as interfaces definidas no arquivo IDL, bem como declarações de encaminhamento para rotinas que os stubs chamam.<br/> |
| Exemplo2 \_ p.c<br/> | O arquivo proxy/stub, que inclui os pontos de entrada substitutos para clientes e para servidores.<br/>                                                                                           |
| Example2 \_ i.c<br/> | O arquivo de ID da interface, que define o GUID para cada interface especificada no arquivo IDL.<br/>                                                                                               |
| Example2.tlb<br/>  | Um arquivo de documento composto que contém informações sobre tipos e objetos.<br/>                                                                                                                |
| Dlldata.c<br/>     | Contém os dados necessários para criar uma DLL de proxy/stub.<br/>                                                                                                                                     |



 

Você usa o arquivo de header e todos os arquivos .c para criar uma [DLL de proxy](building-and-registering-a-proxy-dll.md) que pode dar suporte à interface quando usada por aplicativos cliente e por servidores de objeto. Você usa o arquivo de header da interface (Example2.h) e o arquivo de ID da interface (Exemplo2 i.c) ao criar o arquivo executável para um aplicativo cliente que usa \_ a interface . Você pode optar por incluir o arquivo de biblioteca de tipos como um recurso em seu EXE ou DLL ou pode enviar como um arquivo separado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos gerados para uma interface COM](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[Opções do compilador MIDL](midl-compiler-options.md)
</dt> </dl>

 

