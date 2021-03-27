---
description: Enviado por uma extensão do Gerenciador de arquivos para recuperar informações de unidade da janela do Active File Manager.
title: Mensagem de FM_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988739"
---
# <a name="fm_getdriveinfo-message"></a>Mensagem do FM \_ GETdriveinfo

Enviado por uma extensão do Gerenciador de arquivos para recuperar informações de unidade da janela do Active File Manager.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lpfmsgdi* 
</dt> <dd>

O endereço de uma [**estrutura \_ GetDriveInfo do FMS**](fms-getdriveinfo.md) que recebe informações da unidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero.

## <a name="remarks"></a>Comentários

Se 0xFFFFFFFF for retornado no membro **dwTotalSpace** ou **dwFreeSpace** da estrutura [**\_ GetDriveInfo do FMS**](fms-getdriveinfo.md) , a biblioteca de extensões deverá calcular o valor ou os valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




