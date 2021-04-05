---
description: Habilita ou desabilita a leitura e a gravação de setores de disco.
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
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826281"
---
# <a name="fveenablerawaccessw-function"></a>Função FveEnableRawAccessW

Habilita ou desabilita a leitura e a gravação de setores de disco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeName* \[ no\]
</dt> <dd>

Um identificador exclusivo para o volume do disco.

</dd> <dt>

*Habilitado* \[ no\]
</dt> <dd>

Se **for true**, permitirá o acesso ao volume bruto. Se **for false**, nenhum acesso será permitido para o volume bruto. Se o acesso bruto já tiver sido habilitado, mas esse valor for **false**, o volume será remontado e revalidado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                           | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                           | A função foi bem-sucedida.<br/>                                            |
| <dl> <dt>**S \_ FALSO**</dt> <dt>1 (0x1)</dt> </dl>                        | Habilitado é **falso** e o volume ainda não estava no modo de acesso bruto.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | O volume não pode ser bloqueado.<br/>                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




