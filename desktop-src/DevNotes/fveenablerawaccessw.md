---
description: Habilita ou desabilita a leitura e a escrita de setores de disco.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: Função FveEnableRawAccessW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 050983663b782d40c330092919b8fc29060cbba057a16d147b80c6ea477cbf54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956085"
---
# <a name="fveenablerawaccessw-function"></a>Função FveEnableRawAccessW

Habilita ou desabilita a leitura e a escrita de setores de disco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeName* \[ Em\]
</dt> <dd>

Um identificador exclusivo para o volume de disco.

</dd> <dt>

*Habilitado* \[ Em\]
</dt> <dd>

Se **TRUE**, permitirá o acesso ao volume bruto. Se **FALSE**, nenhum acesso será permitido ao volume bruto. Se o acesso bruto já tiver sido habilitado, mas esse valor for **FALSE,** o volume será remontado e revalidado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retornará um dos códigos a seguir ou outro código de erro se falhar.



| Valor/código de retorno                                                                                                                                                           | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                           | A função foi bem-sucedida.<br/>                                            |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                        | Habilitado é **FALSE** e o volume ainda não estava no modo de acesso bruto.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | O volume não pode ser bloqueado.<br/>                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




