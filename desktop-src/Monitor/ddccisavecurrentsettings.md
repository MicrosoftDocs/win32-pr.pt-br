---
title: Função DDCCISaveCurrentSettings
description: Salva as configurações atuais do monitor no armazenamento não volátil da exibição.
ms.assetid: 293b61d4-36d8-43f4-8800-4dbac3ab11b0
keywords:
- Configuração do monitor de função DDCCISaveCurrentSettings
topic_type:
- apiref
api_name:
- DDCCISaveCurrentSettings
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de590f63acc11ed49dfcdfab6505733da07b508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918250"
---
# <a name="ddccisavecurrentsettings-function"></a>Função DDCCISaveCurrentSettings

> [!IMPORTANT]
> Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo. Os aplicativos não devem chamar essa função.

 

Salva as configurações atuais do monitor no armazenamento não volátil da exibição.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI DDCCISaveCurrentSettings(
   HANDLE hMonitor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMonitor* 
</dt> <dd>

Um identificador para um monitor físico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, ele retornará o **status \_ êxito**. Caso contrário, ele retorna um código de erro **NTSTATUS** .

## <a name="remarks"></a>Comentários

Os aplicativos devem chamar [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) em vez de chamar essa função.

Esta função não tem biblioteca de importação associada. Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Monitorar funções de configuração](monitor-configuration-functions.md)
</dt> </dl>

 

