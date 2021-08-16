---
description: Exibe uma caixa de diálogo que permite aos usuários criar, modificar e excluir perfis de verificação.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'Método IScanProfileUI:: ScanProfileDialog (Scanprofileui. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: a2003471a151677b5f0fbd9ae88e9d3cf8d975525a9dbf8340c6fc1a9f2befc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965805"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>Método IScanProfileUI:: ScanProfileDialog

Exibe uma caixa de diálogo que permite aos usuários criar, modificar e excluir perfis de verificação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Digite: **HWND**

O identificador da janela pai que é proprietária da caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A caixa de diálogo é modal; o usuário não pode alternar para a janela pai até que a caixa de diálogo seja fechada.

Os valores do `<ProfileName>` elemento e do `<WiaItem>` elemento podem ser alterados na caixa de diálogo. O `<Default>` elemento pode ser adicionado ou excluído. Nenhuma outra alteração no perfil de verificação pode ser feita na caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Scanprofileui. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfileUI**](-wia-iscanprofileui.md)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




