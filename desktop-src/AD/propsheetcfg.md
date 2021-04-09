---
title: Estrutura PROPSHEETCFG
description: Usado para conter dados de configuração da folha de propriedades.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory estrutura PROPSHEETCFG
- Active Directory de ponteiro de estrutura de PPROPSHEETCFG
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009404"
---
# <a name="propsheetcfg-structure"></a>Estrutura PROPSHEETCFG

A estrutura **PROPSHEETCFG** é usada para conter dados de configuração da folha de propriedades. Essa estrutura está contida no formato de área de transferência [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) .

> [!Note]  
> Essa estrutura não está definida em um arquivo de cabeçalho publicado. Para usar essa estrutura, você mesmo deve defini-la no formato exato mostrado.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a>Membros

<dl> <dt>

**lNotifyHandle**
</dt> <dd>

Contém o identificador de notificação. Isso é idêntico ao identificador passado para o parâmetro *Handle* no método [**IExtendPropertySheet2:: CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .

</dd> <dt>

**hwndParentSheet**
</dt> <dd>

Contém o identificador de janela da folha de propriedades pai.

</dd> <dt>

**hwndHidden**
</dt> <dd>

Contém o identificador da janela oculta.

</dd> <dt>

**wParamSheetClose**
</dt> <dd>

Contém um valor de 32 bits definido pelo aplicativo. Esse valor é passado de volta para o aplicativo no *wParam* da mensagem [**de \_ \_ notificação de \_ fechamento \_ da folha DSA do WM**](wm-dsa-sheet-close-notify.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[**\_notificação de \_ fechamento da folha DSA \_ do WM \_**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

