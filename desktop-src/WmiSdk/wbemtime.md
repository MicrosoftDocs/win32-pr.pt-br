---
description: A classe WBEMTime facilita conversões entre vários formatos de tempo de execução do Windows e ANSI C. Para obter mais informações, consulte também métodos de classe WBEMTimeSpan.
ms.assetid: b633bc8c-9d02-4bcf-8528-10773fb5ae7a
ms.tgt_platform: multiple
title: Classe WBEMTime (WbemTime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEMTime
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 5d2f06b06db998dc18a876e0e5534e1d86c6ae89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772506"
---
# <a name="wbemtime-class"></a>Classe WBEMTime

\[A classe **WBEMTime** faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

A classe **WBEMTime** facilita conversões entre vários formatos de tempo de execução do Windows e ANSI C. Para obter mais informações, consulte também [**métodos de classe WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan).

## <a name="members"></a>Membros

A classe **WBEMTime** tem estes tipos de membros:

-   [Construtores](#constructors)
-   [Métodos](#methods)

### <a name="constructors"></a>Construtores

A classe **WBEMTime** tem esses construtores.



| Construtor                           | Descrição                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**WBEMTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | Construtor que facilita conversões entre vários formatos de tempo de execução do Windows e ANSI C.<br/> |



 

### <a name="methods"></a>Métodos

A classe **WBEMTime** tem esses métodos.



| Método                                                           | Descrição                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Formatação**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Define a hora no objeto **WBEMTime** como uma hora inválida.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Apresenta o tempo como um valor **BSTR** .<br/>                                                                                      |
| [**GetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Obtém a hora como um valor **BSTR** no formato de data e hora CIM.<br/>                                                                   |
| [**GetDMTFNonNtfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Obtém uma data de DMTF baseada em um FAT ou em um [formato de data e hora](date-and-time-format.md) em que o UTC não é conhecido.<br/> |
| [**GetFILETIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Obtém a hora como uma estrutura **FILETIME** do MFC.<br/>                                                                             |
| [**GetLocalOffsetForDate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Sobrecarregado. Retorna o deslocamento em minutos (+ ou-) entre GMT e hora local para o tempo fornecido no argumento.<br/>         |
| [**GetStructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Obtém a hora como uma estrutura **struct tm** de tempo de execução ANSI C.<br/>                                                                |
| [**GetSystemTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Obtém a hora como uma estrutura **SYSTEMTIME** do MFC.<br/>                                                                           |
| [**GetTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Obtém a hora como um inteiro de 64 bits.<br/>                                                                                          |
| [**GetTime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Obtém a hora como uma variável t de tempo de execução ANSI C \_ .<br/>                                                                       |
| [**IsOk**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Indica se o objeto **WBEMTime** representa uma hora válida.<br/>                                                          |
| [**SetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Define a hora no objeto **WBEMTime** no formato de data e hora CIM.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>Operadores sobrecarregados do WBEMTime

O objeto **WBEMTime** define os seguintes operadores sobrecarregados.



| Operadores sobrecarregados do WBEMTime                                                                                                                                                                                                                                                                                                                                                                                                                                        | Descrição                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**operador =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | O operador de *atribuição* facilita as conversões entre vários formatos de tempo de execução do Windows e ANSI C.                           |
| [**operador +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | O operador de *adição* incrementa o tempo de um objeto por um período de tempo. O resultado é retornado em um novo objeto **WBEMTime** .              |
| [**operador + =**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | O operador *Add-e-Assign* incrementa o tempo de um objeto por um período de tempo.                                                             |
| [**operador**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | O operador de *subtração* decrementa a hora de um objeto por outro tempo do objeto. O resultado é retornado em um novo objeto **WBEMTime** . |
| [**operador-=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | O operador *subtrair e atribuir* diminui a hora de um objeto por um período de tempo.                                                        |
| [**operador = =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)[**operador! =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**>do operador**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**>do operador =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**<do operador**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**<do operador =**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Os operadores de comparação comparam dois objetos **WBEMTime** .                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



 

