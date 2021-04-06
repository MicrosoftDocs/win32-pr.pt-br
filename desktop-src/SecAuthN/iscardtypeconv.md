---
description: Fornece os métodos necessários para dar suporte aos usuários das outras interfaces COM de cartão inteligente.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interface ISCardTypeConv (Scarddat. h)
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
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828349"
---
# <a name="iscardtypeconv-interface"></a>Interface ISCardTypeConv

\[A interface **ISCardTypeConv** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A interface **ISCardTypeConv** fornece os métodos necessários para dar suporte aos usuários das outras interfaces com de [*cartão inteligente*](../secgloss/s-gly.md) . Essa interface é fornecida apenas para fins de compatibilidade com versões anteriores e não deve mais ser usada.

## <a name="members"></a>Membros

A interface **ISCardTypeConv** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardTypeConv** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardTypeConv** tem esses métodos.



| Método                                                                              | Descrição                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertByteArrayToByteBuffer**](iscardtypeconv-convertbytearraytobytebuffer.md) | Converte uma matriz de bytes C/C++ típica em um buffer universal de bytes (objeto **IStream** ).<br/>                                   |
| [**ConvertByteBufferToByteArray**](iscardtypeconv-convertbytebuffertobytearray.md) | Converte uma matriz de bytes mapeada em um buffer universal de bytes (objeto **IStream** ) em uma matriz de bytes C/C++ típica.<br/>          |
| [**ConvertByteBufferToSafeArray**](iscardtypeconv-convertbytebuffertosafearray.md) | Converte uma matriz de bytes mapeada em um buffer universal de bytes (objeto **IStream** ) em um SafeArray de Char (Byte) não assinado.<br/> |
| [**ConvertSafeArrayToByteBuffer**](iscardtypeconv-convertsafearraytobytebuffer.md) | Converte uma matriz de bytes definida como um SAFEARRAY em um buffer universal de bytes (objeto **IStream** ).<br/>                          |
| [**CreateByteArray**](iscardtypeconv-createbytearray.md)                           | Cria uma matriz de bytes.<br/>                                                                                                   |
| [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)                         | Cria um buffer universal de bytes mapeados em um objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)).<br/>                  |
| [**Createsafearray**](iscardtypeconv-createsafearray.md)                           | Cria um SAFEARRAY de automação de caracteres não assinados (bytes).<br/>                                                              |
| [**FreeIStreamMemoryPtr**](iscardtypeconv-freeistreammemoryptr.md)                 | Libera um ponteiro de memória para o bloco de memória HGLOBAL gerenciado por uma interface com de **IStream** .<br/>                                  |
| [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)                     | Adquire um ponteiro de byte para o bloco de memória HGLOBAL que é gerenciado pela interface com de **IStream** .<br/>                        |
| [**SizeOfIStream**](iscardtypeconv-sizeofistream.md)                               | Determina o tamanho (número de bytes) de uma interface com com **IStream** .<br/>                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



 

 
