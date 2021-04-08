---
description: A interface IByteBuffer é fornecida para ler, gravar e gerenciar objetos Stream. Esse objeto essencialmente é um wrapper para o objeto IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interface IByteBuffer (Scardssp. h)
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
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922523"
---
# <a name="ibytebuffer-interface"></a>Interface IByteBuffer

\[A interface **IByteBuffer** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]

A interface **IByteBuffer** é fornecida para ler, gravar e gerenciar objetos Stream. Esse objeto essencialmente é um wrapper para o objeto **IStream** .

## <a name="members"></a>Membros

A interface **IByteBuffer** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IByteBuffer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IByteBuffer** tem esses métodos.



| Método                                           | Descrição                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**8i**](ibytebuffer-clone.md)               | Clona um objeto **IByteBuffer** .<br/>                                                              |
| [**Compromisso**](ibytebuffer-commit.md)             | Confirma uma [*transação*](/windows/desktop/SecGloss/t-gly).<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | Copia bytes para outro objeto.<br/>                                                                |
| [**Inicializar**](ibytebuffer-initialize.md)     | Inicializa o objeto **IByteBuffer** .<br/>                                                        |
| [**LockRegion**](ibytebuffer-lockregion.md)     | Restringe o acesso a um intervalo de bytes.<br/>                                                          |
| [**Ler**](ibytebuffer-read.md)                 | Lê bytes na memória.<br/>                                                                       |
| [**Voltar**](ibytebuffer-revert.md)             | Descarta as alterações desde a última chamada de [**confirmação**](ibytebuffer-commit.md) .<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | Altera o ponteiro de busca.<br/>                                                                      |
| [**Size**](ibytebuffer-setsize.md)           | Altera o tamanho do objeto de fluxo.<br/>                                                         |
| [**Stat**](ibytebuffer-stat.md)                 | Recupera informações estatísticas sobre um fluxo.<br/>                                              |
| [**UnlockRegion**](ibytebuffer-unlockregion.md) | Remove a restrição de acesso definida anteriormente por [**LockRegion**](ibytebuffer-lockregion.md).<br/>     |
| [**Gravar**](ibytebuffer-write.md)               | Grava bytes no fluxo.<br/>                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

