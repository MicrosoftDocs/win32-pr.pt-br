---
description: Fornece os métodos necessários para dar suporte aos usuários das outras interfaces COM de cartão inteligente.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interface ISCardTypeConv (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7fbf009eeeb4f104e5bf09ba8e33b6b2b76eb889a0e44e7594172c697b438d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013586"
---
# <a name="iscardtypeconv-interface"></a>Interface ISCardTypeConv

\[A interface **ISCardTypeConv** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A interface **ISCardTypeConv** fornece os métodos necessários para dar suporte aos usuários das [*outras*](../secgloss/s-gly.md) interfaces COM de cartão inteligente. Essa interface é fornecida apenas para compatibilidade com backward e não deve mais ser usada.

## <a name="members"></a>Membros

A interface **ISCardTypeConv** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardTypeConv** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardTypeConv** tem esses métodos.



| Método                                                                              | Descrição                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertByteArrayToByteBuffer**](iscardtypeconv-convertbytearraytobytebuffer.md) | Converte uma matriz de bytes C/C++ típica em um buffer universal de bytes (**objeto IStream).**<br/>                                   |
| [**ConvertByteBufferToByteArray**](iscardtypeconv-convertbytebuffertobytearray.md) | Converte uma matriz de bytes mapeada em um buffer universal de bytes (**objeto IStream)** em uma matriz de bytes C/C++ típica.<br/>          |
| [**ConvertByteBufferToSafeArray**](iscardtypeconv-convertbytebuffertosafearray.md) | Converte uma matriz de bytes mapeada em um buffer universal de bytes (**objeto IStream)** em um SAFEARRAY de caractere não assinado (byte).<br/> |
| [**ConvertSafeArrayToByteBuffer**](iscardtypeconv-convertsafearraytobytebuffer.md) | Converte uma matriz de bytes definida como SAFEARRAY em um buffer universal de bytes (**objeto IStream).**<br/>                          |
| [**CreateByteArray**](iscardtypeconv-createbytearray.md)                           | Cria uma matriz de bytes.<br/>                                                                                                   |
| [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)                         | Cria um buffer universal de bytes mapeados em **um objeto IStream** ([**IByteBuffer**](ibytebuffer.md)).<br/>                  |
| [**CreateSafeArray**](iscardtypeconv-createsafearray.md)                           | Cria uma SAFEARRAY de Automação de caracteres não assinados (bytes).<br/>                                                              |
| [**FreeIStreamMemoryPtr**](iscardtypeconv-freeistreammemoryptr.md)                 | Libera um ponteiro de memória para o bloco de memória HGLOBAL gerenciado por uma interface COM **IStream.**<br/>                                  |
| [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)                     | Adquire um ponteiro de byte para o bloco de memória HGLOBAL que é gerenciado pela interface COM **do IStream.**<br/>                        |
| [**SizeOfIStream**](iscardtypeconv-sizeofistream.md)                               | Determina o tamanho (número de bytes) de uma interface **COM IStream.**<br/>                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardTypeConv é definido como \_ 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



 

 
