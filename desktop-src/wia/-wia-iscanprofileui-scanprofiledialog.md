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
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169539"
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

Tipo: **HWND**

O identificador da janela pai que é proprietária da caixa de diálogo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A caixa de diálogo é modal; o usuário não pode alternar para a janela pai até que a caixa de diálogo seja fechada.

Os valores do `<ProfileName>` elemento e do `<WiaItem>` elemento podem ser alterados na caixa de diálogo. O `<Default>` elemento pode ser adicionado ou excluído. Nenhuma outra alteração no perfil de verificação pode ser feita na caixa de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Scanprofileui. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfileUI**](-wia-iscanprofileui.md)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




