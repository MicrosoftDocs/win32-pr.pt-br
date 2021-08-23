---
description: Um handle para um buffer de cadeia de caracteres mutável que você pode usar para criar um HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (Hstring.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f115ca18b4bf5b81bbd7004259aa525517c05a3adc0f6376f7d16df3e3ce679
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733816"
---
# <a name="hstring_buffer"></a>HSTRING \_ BUFFER

Um handle para um buffer de cadeia de caracteres mutável que você pode usar para criar um [**HSTRING.**](hstring.md)


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Comentários

**HSTRING \_ BUFFER** representa um buffer de cadeia de caracteres que você pode modificar antes de convertê-lo em um [**HSTRING imutável.**](hstring.md)

Chame a [**função WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para criar um **\_ BUFFER HSTRING.** Chame [**o WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para converter um **\_ BUFFER HSTRING** em um [**HSTRING imutável.**](hstring.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Hstring.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
