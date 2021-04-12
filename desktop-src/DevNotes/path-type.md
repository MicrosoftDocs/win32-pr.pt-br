---
description: Representa o tipo de caminho que está sendo usado como um argumento.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Enumeração de PATH_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500775"
---
# <a name="path_type-enumeration"></a>Enumeração de tipo de caminho \_

Representa o tipo de caminho que está sendo usado como um argumento.

## <a name="syntax"></a>Syntax


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOS_PATH"></span><span id="dos_path"></span>**\_caminho dos**
</dt> <dd>

Caminho padrão.

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**caminho do NT \_**
</dt> <dd>

Caminho interno.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




