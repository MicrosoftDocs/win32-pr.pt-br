---
description: Um identificador para um buffer de cadeia de caracteres mutável que você pode usar para criar um HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783734"
---
# <a name="hstring_buffer"></a>\_buffer HSTRING

Um identificador para um buffer de cadeia de caracteres mutável que você pode usar para criar um [**HSTRING**](hstring.md).


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Comentários

**HSTRING \_ BUFFER** representa um buffer de cadeia de caracteres que você pode modificar antes de convertê-lo em um [**HSTRING**](hstring.md)imutável.

Chame a função [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para criar um **\_ buffer HSTRING**. Chame o [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para converter um **\_ buffer HSTRING** em uma [**HSTRING**](hstring.md)imutável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Hstring. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
