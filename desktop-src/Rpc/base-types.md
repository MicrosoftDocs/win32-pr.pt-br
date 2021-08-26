---
title: Tipos base
description: Para evitar os problemas que os tipos de dados dependentes de implementação podem causar em diferentes arquiteturas de computador, o MIDL define seus próprios tipos de dados base.
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aadc1ae5fedd73a01ce0fd7ed735689e043cff0d74910175cf2ab691c22eeed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023276"
---
# <a name="base-types"></a>Tipos base

Para evitar os problemas que os tipos de dados dependentes de implementação podem causar em diferentes arquiteturas de computador, o MIDL define seus próprios tipos de dados base.



| Tipo base                         | Descrição                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Boolean**](/windows/desktop/Midl/boolean)       | Um item de dados que pode ter o **valor TRUE** ou **FALSE.**                                                                                                          |
| [**Byte**](/windows/desktop/Midl/byte)             | Um item de dados de 8 bits com garantia de ser transmitido sem nenhuma alteração.                                                                                                 |
| [**char**](/windows/desktop/Midl/char-idl)         | Um item de dados de caractere sem assinatura de 8 bits.                                                                                                                              |
| [**Duplo**](/windows/desktop/Midl/double)         | Um número de ponto flutuante de 64 bits.                                                                                                                                     |
| [**Flutuar**](/windows/desktop/Midl/float)           | Um número de ponto flutuante de 32 bits.                                                                                                                                     |
| [**handle \_ t**](/windows/desktop/Midl/handle-t)    | Um alça primitivo que pode ser usado para associação RPC ou serialização de dados.                                                                                            |
| [**Hyper**](/windows/desktop/Midl/hyper)           | Um inteiro de 64 bits que [](/windows/desktop/Midl/signed) pode [](/windows/desktop/Midl/unsigned) ser declarado como assinado ou não assinado também pode ser chamado **\_ de int64.**                  |
| [**INT**](/windows/desktop/Midl/int)               | Um inteiro de 32 bits que pode ser declarado como **assinado** ou **sem sinal.**                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | Uma palavra-chave que especifica um tipo integral que tem propriedades de 32 ou 64 bits.                                                                              |
| [**long**](/windows/desktop/Midl/long)             | Um modificador para **int** que indica um inteiro de 32 bits. Pode ser declarado como assinado **ou** **sem assinatura.**                                                       |
| [**short**](/windows/desktop/Midl/short)           | Um inteiro de 16 bits que pode ser declarado como **assinado** ou **sem sinal.**                                                                                         |
| [**Pequeno**](/windows/desktop/Midl/small)           | Um modificador para **int** que indica um inteiro de 8 bits. Pode ser declarado como assinado **ou** **sem assinatura.**                                                       |
| [**wchar \_ t**](/windows/desktop/Midl/wchar-t)      | Tipo de caractere largo com suporte como uma extensão da Microsoft para IDL. Portanto, esse tipo não estará disponível se você compilar usando a [ / **opção osf.**](/windows/desktop/Midl/-osf) |



 

O arquivo de header Rpcndr.h fornece definições para a maioria desses tipos de dados base. A **palavra-chave int** é reconhecida e é transmitível em plataformas de 32 bits. Em plataformas de 16 bits, o tipo de dados **int** requer um modificador, como **curto** ou **longo,** para especificar seu comprimento.

Embora **\* \* void** seja reconhecido como um tipo de ponteiro genérico pelo padrão ANSI C, MIDL restringe seu uso. Cada ponteiro usado em uma operação remota ou serialização deve apontar para tipos base ou tipos construídos de tipos base. (Há uma exceção: os alças de contexto são definidos como **tipos nulos.** Para obter mais informações, consulte [Context Handles](context-handles.md).)

 

 