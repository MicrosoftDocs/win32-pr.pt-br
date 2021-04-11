---
title: Tipos base
description: Para evitar os problemas que os tipos de dados dependentes de implementação podem causar em diferentes arquiteturas de computador, MIDL define seus próprios tipos de dados base.
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee57261aac1de6ea4bb15c9a4550721dd10282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294429"
---
# <a name="base-types"></a>Tipos base

Para evitar os problemas que os tipos de dados dependentes de implementação podem causar em diferentes arquiteturas de computador, MIDL define seus próprios tipos de dados base.



| Tipo base                         | Descrição                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**booleano**](/windows/desktop/Midl/boolean)       | Um item de dados que pode ter o valor **true** ou **false**.                                                                                                          |
| [**minuciosa**](/windows/desktop/Midl/byte)             | Um item de dados de 8 bits garantido para ser transmitido sem nenhuma alteração.                                                                                                 |
| [**char**](/windows/desktop/Midl/char-idl)         | Um item de dados de caractere sem sinal de 8 bits.                                                                                                                              |
| [**double**](/windows/desktop/Midl/double)         | Um número de ponto flutuante de 64 bits.                                                                                                                                     |
| [**float**](/windows/desktop/Midl/float)           | Um número de ponto flutuante de 32 bits.                                                                                                                                     |
| [**lidar com \_ t**](/windows/desktop/Midl/handle-t)    | Um identificador primitivo que pode ser usado para associação RPC ou serialização de dados.                                                                                            |
| [**Hyper**](/windows/desktop/Midl/hyper)           | Um inteiro de 64 bits que pode ser declarado como [**assinado**](/windows/desktop/Midl/signed) ou [**não assinado**](/windows/desktop/Midl/unsigned) também pode ser referido como **\_ Int64**.                  |
| [**int**](/windows/desktop/Midl/int)               | Um inteiro de 32 bits que pode ser declarado como **assinado** ou **não assinado**.                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | Uma palavra-chave que especifica um tipo integral que tem propriedades de 32 bits ou 64 bits.                                                                              |
| [**Longas**](/windows/desktop/Midl/long)             | Um modificador para **int** que indica um inteiro de 32 bits. Pode ser declarado como **assinado** ou **não assinado**.                                                       |
| [**short**](/windows/desktop/Midl/short)           | Um inteiro de 16 bits que pode ser declarado como **assinado** ou **não assinado**.                                                                                         |
| [**menores**](/windows/desktop/Midl/small)           | Um modificador para **int** que indica um inteiro de 8 bits. Pode ser declarado como **assinado** ou **não assinado**.                                                       |
| [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)      | Tipo de caractere largo com suporte como uma extensão da Microsoft para IDL. Portanto, esse tipo não estará disponível se você compilar usando a opção [ / **uso**](/windows/desktop/Midl/-osf) |



 

O arquivo de cabeçalho Rpcndr. h fornece definições para a maioria desses tipos de dados base. A palavra-chave **int** é reconhecida e é transmititable em plataformas de 32 bits. Em plataformas de 16 bits, o tipo de dados **int** requer um modificador, como **curto** ou **longo**, para especificar seu comprimento.

Embora **void \* \*** seja reconhecido como um tipo de ponteiro genérico pelo padrão ANSI C, o MIDL restringe seu uso. Cada ponteiro usado em uma operação remota ou de serialização deve apontar para tipos base ou tipos construídos a partir de tipos base. (Há uma exceção: os identificadores de contexto são definidos como tipos **void** . Para obter mais informações, consulte [identificadores de contexto](context-handles.md).)

 

 