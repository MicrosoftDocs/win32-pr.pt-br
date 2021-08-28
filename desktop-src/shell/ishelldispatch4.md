---
description: Estende o objeto IShellDispatch3.
title: Objeto IShellDispatch4 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: 057ef4082bac8d04c006d951db7d2d251be2f8c62e88af65bc1a69678514af81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969005"
---
# <a name="ishelldispatch4-object"></a>Objeto IShellDispatch4

Estende o objeto [**IShellDispatch3**](ishelldispatch3.md) . Além das propriedades e métodos com suporte do **IShellDispatch3**, o **IShellDispatch4** dá suporte a quatro métodos adicionais.

> [!Note]  
> **IShellDispatch4** é implementado e acessado por meio do objeto [**shell**](shell.md) .

 

## <a name="members"></a>Membros

O objeto **IShellDispatch4** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **IShellDispatch4** tem esses métodos.



| Método                                                     | Descrição                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | Obtém o valor de uma política especificada do Internet Explorer.<br/> |
| [**GetDefinition**](ishelldispatch4-getsetting.md)           | Recupera uma configuração de shell global.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Exibe ou oculta a área de trabalho.<br/>                           |
| [**WindowsSecurity**](ishelldispatch4-windowssecurity.md) | exibe a caixa de diálogo **Segurança do Windows** .<br/>            |



 

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
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> </dl>

 

 
