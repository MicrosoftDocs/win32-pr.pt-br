---
title: CFSTR_DSOP_DS_SELECTION_LIST (Objsel. h)
description: O formato da área de transferência da lista de seleção do CFSTR \_ DSOP \_ DS fornece um \_ \_ HGLOBAL que contém uma estrutura de lista de seleção do DS \_ \_ . A estrutura da lista de seleção do DS \_ \_ contém dados sobre os itens selecionados em uma caixa de diálogo Seletor de objetos de diretório.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918288"
---
# <a name="cfstr_dsop_ds_selection_list"></a>lista de seleção do CFSTR \_ DSOP \_ DS \_ \_

<dl> <dt>

<span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**lista de seleção do CFSTR \_ DSOP \_ DS \_ \_**
</dt> <dd> <dl> <dt>

"lista de seleção do CFSTR \_ DSOP \_ DS \_ \_ "
</dt> <dt>



O formato da área de transferência da **lista de seleção do CFSTR \_ DSOP \_ \_ \_ DS** é fornecido pelo [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtido chamando [**IDsObjectPicker:: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog). O formato da área de transferência da **lista de seleção do CFSTR \_ DSOP \_ \_ \_ DS** fornece um **HGLOBAL** que contém uma estrutura de [**\_ \_ lista de seleção do DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) . A estrutura da **\_ \_ lista de seleção do DS** contém dados sobre os itens selecionados em uma caixa de diálogo [seletor de objetos de diretório](directory-object-picker.md) .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Objsel. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_lista de seleção de DS \_**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[Seletor de objetos de diretório](directory-object-picker.md)
</dt> </dl>

 

