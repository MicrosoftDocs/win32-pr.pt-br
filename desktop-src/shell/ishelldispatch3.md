---
description: Estende o objeto IShellDispatch2.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: Objeto IShellDispatch3 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8f02095415ff2682e1f2a2eeb21c4afe0754b72251f6129856f1b6a415913cf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720912"
---
# <a name="ishelldispatch3-object"></a>Objeto IShellDispatch3

Estende o objeto [**IShellDispatch2**](ishelldispatch2-object.md) . O **IShellDispatch3** dá suporte a um novo método além das propriedades e métodos com suporte do **IShellDispatch2**.

> [!Note]  
> **IShellDispatch3** é implementado e acessado por meio do objeto [**shell**](shell.md) .

 

## <a name="members"></a>Membros

O objeto **IShellDispatch3** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **IShellDispatch3** tem esses métodos.



| Método                                             | Descrição                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [**AddToRecent**](ishelldispatch3-addtorecent.md) | Adiciona um arquivo à lista MRU (usada mais recentemente).<br/> |



 

## <a name="remarks"></a>Comentários

para obter uma discussão sobre os serviços de Windows, consulte a documentação de [serviços](../services/services.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 6,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> </dl>

 

 
