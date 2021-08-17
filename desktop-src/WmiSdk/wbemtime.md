---
description: A classe WBEMTime facilita conversões entre vários formatos de tempo de execução Windows e ANSI C. Para obter mais informações, consulte também Métodos de classe WBEMTimeSpan.
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
ms.openlocfilehash: 16b4e8933113386e877aec23313f74695b321f932c10f0e2730bcf5888675cc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553240"
---
# <a name="wbemtime-class"></a>Classe WBEMTime

\[A **classe WBEMTime** faz parte do WMI Provider Framework, que agora é considerado no estado final e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estará disponível para problemas não relacionados à segurança que afetam essas bibliotecas. As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

A **classe WBEMTime** facilita conversões entre vários formatos de tempo de execução Windows e ANSI C. Para obter mais informações, consulte também Métodos de classe [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan).

## <a name="members"></a>Membros

A **classe WBEMTime** tem estes tipos de membros:

-   [Construtores](#constructors)
-   [Métodos](#methods)

### <a name="constructors"></a>Construtores

A **classe WBEMTime** tem esses construtores.



| Construtor                           | Descrição                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**WBEMTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | Construtor que facilita conversões entre vários Windows e formatos de tempo de run time anSI C.<br/> |



 

### <a name="methods"></a>Métodos

A **classe WBEMTime** tem esses métodos.



| Método                                                           | Descrição                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Limpar**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Define a hora no **objeto WBEMTime** como uma hora inválida.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Apresenta a hora como um **valor BSTR.**<br/>                                                                                      |
| [**GetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Obtém a hora como um **valor BSTR** no formato datetime cim.<br/>                                                                   |
| [**GetDMTFNonNtfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Obtém uma data DMTF baseada em um FAT ou um formato de data e [hora](date-and-time-format.md) em que o UTC não é conhecido.<br/> |
| [**Getfiletime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Obtém a hora como uma estrutura **FILETIME MFC.**<br/>                                                                             |
| [**GetLocalOffsetForDate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Sobrecarregado. Retorna o deslocamento em minutos(+ ou -) entre GMT e hora local para a hora fornecida no argumento .<br/>         |
| [**GetStructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Obtém o tempo como uma estrutura tm de **struct** de tempo de run time anSI C.<br/>                                                                |
| [**Getsystemtime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Obtém a hora como uma estrutura **SYSTEMTIME MFC.**<br/>                                                                           |
| [**Gettime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Obtém a hora como um inteiro de 64 bits.<br/>                                                                                          |
| [**Gettime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Obtém o tempo como uma variável t de tempo de run time do ANSI \_ C.<br/>                                                                       |
| [**IsOk**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Indica se o **objeto WBEMTime** representa uma hora válida.<br/>                                                          |
| [**SetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Define a hora no objeto **WBEMTime** no formato datetime CIM.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>Operadores sobrecarregados WBEMTime

O **objeto WBEMTime** define os seguintes operadores sobrecarregados.



| Operadores sobrecarregados WBEMTime                                                                                                                                                                                                                                                                                                                                                                                                                                        | Descrição                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**operator =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *O* operador de atribuição facilita conversões entre vários Windows formatos de tempo de run time do ANSI C.                           |
| [**operador +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | *O* operador de adição incrementa o tempo de um objeto por um período de tempo. O resultado é retornado em um novo **objeto WBEMTime.**              |
| [**operator +=**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | *O operador add-and-assign* incrementa o tempo de um objeto por um período de tempo.                                                             |
| [**operador –**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *O operador* de subtração diminui o tempo de um objeto pelo tempo de outro objeto. O resultado é retornado em um novo **objeto WBEMTime.** |
| [**operator -=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | *O operador subtract-and-assign* diminui o tempo de um objeto por um período de tempo.                                                        |
| [**operador ==**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)[**operador !=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**operador >**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**operator >=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**operador <**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**operator <=**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Os operadores de comparação comparam dois **objetos WBEMTime.**                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



 

