---
description: Define o perfil de verificação especificado como o perfil padrão.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'Método IScanProfileMgr:: SetDefault (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811773"
---
# <a name="iscanprofilemgrsetdefault-method"></a>Método IScanProfileMgr:: SetDefault

Define o perfil de verificação especificado como o perfil padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pScanProfile* \[ no\]
</dt> <dd>

Tipo: **[**IScanProfile**](-wia-iscanprofile.md) \** _

Um ponteiro para o perfil.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Use o método **IScanProfileMgr:: SetDefault** para adicionar um `<Default>` elemento ao perfil ou para remover esse elemento do perfil padrão anterior do dispositivo.

Use o método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) para alterar o perfil padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Esquema do perfil de verificação](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




