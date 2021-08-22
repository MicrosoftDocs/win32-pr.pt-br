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
ms.openlocfilehash: d1307747fca18cd1cd86d13c5718240bff260d0882a6865bd817d44632093e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013454"
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

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará o **status \_ êxito**. Caso contrário, ele retorna um código de erro **NTSTATUS** .

## <a name="remarks"></a>Comentários

Os aplicativos devem chamar [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) em vez de chamar essa função.

Esta função não tem biblioteca de importação associada. Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Monitorar funções de configuração](monitor-configuration-functions.md)
</dt> </dl>

 

