---
description: As classes a seguir são declaradas e associadas a identificadores de classe (CLSIDs) em wmcodecdsp. h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificadores de classe para o analisador de Sumário (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758709"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a>Identificadores de classe para o analisador de Sumário

As classes a seguir são declaradas e associadas a identificadores de classe (CLSIDs) em wmcodecdsp. h.



| Nome da classe       | Nome amigável do objeto |
|------------------|----------------------|
| CTocEntry        | Entrada de Sumário            |
| CTocEntryList    | Lista de entradas de Sumário       |
| CToc             | SUMÁRIO                  |
| CTocCollection   | Coleção de SUMÁRIOs       |
| CTocParser       | Analisador de Sumário           |
| CTocGeneratorDmo | Gerador de Sumário        |



 

A tabela anterior fornece um nome de objeto amigável para cada classe. Esta documentação usa esses nomes amigáveis para se referir a instâncias das classes. Por exemplo, a documentação refere-se a uma instância da classe CTocEntry como um objeto de entrada de Sumário.

No código, você pode usar **\_ \_ uuidof** para se referir aos CLSIDs. Por exemplo, você pode usar o código a seguir para se referir ao CLSID para CTocGeneratorDmo.


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a>Constantes de CLSID definidas em Wmcodecdsp. h

Como alternativa ao uso de **\_ \_ uuidof**, você pode usar constantes para se referir aos CLSIDs. As constantes a seguir são definidas em wmcodecdsp. h



| Nome da classe     | Constante de CLSID        |
|----------------|-----------------------|
| CTocEntry      | \_CTOCENTRY CLSID      |
| CTocEntryList  | \_CTOCENTRYLIST CLSID  |
| CToc           | \_CTOC CLSID           |
| CTocCollection | \_CTOCCOLLECTION CLSID |
| CTocParser     | \_CTOCPARSER CLSID     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a>Constantes de CLSID definidas em Wmcodecdspuuid. lib

A constante de CLSID a seguir é declarada, mas não definida, em wmcodecdsp. h. Para usá-lo no código, você deve vincular a wmcodecdspuuid. lib.



| Nome da classe       | Constante de CLSID          |
|------------------|-------------------------|
| CTocGeneratorDmo | \_CTOCGENERATORDMO CLSID |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmvdspa.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do analisador de Sumário](toc-parser-objects.md)
</dt> </dl>

 

 




