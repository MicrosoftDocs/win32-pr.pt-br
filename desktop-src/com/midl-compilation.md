---
title: Compilação de MIDL
description: Compilação de MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454371"
---
# <a name="midl-compilation"></a>Compilação de MIDL

Dado um arquivo IDL, como [example2. idl](anatomy-of-an-idl-file.md), que define uma ou mais interfaces com e uma biblioteca de tipos, o compilador MIDL (Midl.exe) gera os arquivos descritos na tabela a seguir como a saída padrão.



| Nome de arquivo                 | Descrição                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Example2. h<br/>    | O arquivo de cabeçalho, que contém definições de tipo e declarações de função para todas as interfaces definidas no arquivo IDL, bem como declarações de encaminhamento para rotinas que os stubs chamam.<br/> |
| Example2 \_ p. c<br/> | O arquivo de proxy/stub, que inclui os pontos de entrada substitutos para clientes e para servidores.<br/>                                                                                           |
| Example2 \_ i. c<br/> | O arquivo de ID de interface, que define o GUID para cada interface especificada no arquivo IDL.<br/>                                                                                               |
| Example2. tlb<br/>  | Um arquivo de documento composto que contém informações sobre tipos e objetos.<br/>                                                                                                                |
| Dlldata. c<br/>     | Contém os dados necessários para criar uma DLL de proxy/stub.<br/>                                                                                                                                     |



 

Você usa o arquivo de cabeçalho e todos os arquivos. c para [criar uma DLL de proxy](building-and-registering-a-proxy-dll.md) que pode dar suporte à interface quando usada por aplicativos cliente e por servidores de objetos. Você usa o arquivo de cabeçalho de interface (example2. h) e o arquivo de ID de interface (example2 \_ i. c) ao criar o arquivo executável para um aplicativo cliente que usa a interface. Você pode optar por incluir o arquivo de biblioteca de tipos como um recurso em seu EXE ou DLL, ou pode enviá-lo como um arquivo separado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquivos gerados para uma interface COM](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[Opções do compilador MIDL](midl-compiler-options.md)
</dt> </dl>

 

