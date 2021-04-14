---
description: Executa a inicialização necessária para permitir que o aplicativo de chamada se torne um coletor de vídeo Miracast.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Função WFDDisplaySinkStart (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502357"
---
# <a name="wfddisplaysinkstart-function"></a>Função WFDDisplaySinkStart

Executa a inicialização necessária para permitir que o aplicativo de chamada se torne um coletor de vídeo Miracast. Seu aplicativo deve chamá-lo uma vez na inicialização.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uDeviceCategory* \[ no\]
</dt> <dd>

A categoria do dispositivo.

</dd> <dt>

*uSubCategory* \[ no\]
</dt> <dd>

A subcategoria do dispositivo.

</dd> <dt>

*pCallbackContext* \[ em, opcional\]
</dt> <dd>

Um ponteiro de contexto opcional que é passado para a função de retorno de chamada especificada no parâmetro *pfnCallback* .

</dd> <dt>

*pfnCallback* \[ no\]
</dt> <dd>

Um ponteiro para a função de retorno de chamada a ser chamado sempre que houver uma notificação para o aplicativo. As notificações que podem ser enviadas são descritas em [**retorno de chamada de notificação do \_ coletor de vídeo \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser um dos códigos de retorno a seguir.



| Código de retorno                                                                                          | Descrição                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**ERRO \_ sem \_ suporte**</dt> </dl> | Não há suporte para o coletor de vídeo neste hardware.<br/> |



 

## <a name="remarks"></a>Comentários

Essa função executa as seguintes tarefas:

-   Torna o PC detectável
-   Define as informações do dispositivo P2P para refletir a categoria e a subcategoria especificadas
-   Define o Miracast s em todos os Wi-Fi quadros diretos com o tipo de dispositivo como o coletor
-   Registra o retorno de chamada especificado a ser invocado sempre que houver uma conexão de entrada

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows 10<br/>                                                                      |
| Fim do suporte do servidor<br/>    | Windows Server 2016<br/>                                                             |
| parâmetro<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_retorno de \_ chamada de notificação do coletor de vídeo WFD \_ \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




