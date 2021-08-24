---
description: A interface IByteBuffer é fornecida para ler, gravar e gerenciar objetos de fluxo. Esse objeto é essencialmente um wrapper para o objeto IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interface IByteBuffer (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8f0aa81106629142efeec7e22bdb495bea853c3c689d6b55887a62f896d89d62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417406"
---
# <a name="ibytebuffer-interface"></a>Interface IByteBuffer

\[A interface **IByteBuffer** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

A interface **IByteBuffer** é fornecida para ler, gravar e gerenciar objetos de fluxo. Esse objeto é essencialmente um wrapper para o **objeto IStream.**

## <a name="members"></a>Membros

A interface **IByteBuffer** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IByteBuffer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IByteBuffer** tem esses métodos.



| Método                                           | Descrição                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Clone**](ibytebuffer-clone.md)               | Clona **um objeto IByteBuffer.**<br/>                                                              |
| [**Commit**](ibytebuffer-commit.md)             | Confirma uma [*transação*](/windows/desktop/SecGloss/t-gly).<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | Copia bytes para outro objeto.<br/>                                                                |
| [**Inicializar**](ibytebuffer-initialize.md)     | Inicializa o objeto **IByteBuffer.**<br/>                                                        |
| [**Lockregion**](ibytebuffer-lockregion.md)     | Restringe o acesso a um intervalo de bytes.<br/>                                                          |
| [**Ler**](ibytebuffer-read.md)                 | Lê bytes na memória.<br/>                                                                       |
| [**Reverter**](ibytebuffer-revert.md)             | Descarta as alterações desde a última [**chamada de**](ibytebuffer-commit.md) Confirmação.<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | Altera o ponteiro de busca.<br/>                                                                      |
| [**Setsize**](ibytebuffer-setsize.md)           | Altera o tamanho do objeto de fluxo.<br/>                                                         |
| [**Stat**](ibytebuffer-stat.md)                 | Recupera informações estatísticas sobre um fluxo.<br/>                                              |
| [**Unlockregion**](ibytebuffer-unlockregion.md) | Remove a restrição de acesso definida anteriormente [**por LockRegion.**](ibytebuffer-lockregion.md)<br/>     |
| [**Gravar**](ibytebuffer-write.md)               | Grava bytes no fluxo.<br/>                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID IByteBuffer é definido como \_ E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

