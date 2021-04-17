---
description: Cria um manipulador de fluxo de bytes para a origem de mídia MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: Função MFCreateMP3ByteStreamPlugin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754421"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a>Função MFCreateMP3ByteStreamPlugin

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro. Em vez disso, os aplicativos devem usar o [resolvedor de origem](source-resolver.md) para criar a origem de mídia mp3.\]

Cria um manipulador de fluxo de bytes para a origem de mídia MP3.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* \[ no\]
</dt> <dd>

O IID (identificador de interface) da interface solicitada. Defina esse parâmetro como **IID \_ IMFByteStreamHandler** para receber um ponteiro para a interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .

</dd> <dt>

*ppvHandler* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface. O chamador deve liberar a interface.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação associada. Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a mf.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |
| Fim do suporte do cliente<br/>    | Windows Vista<br/>                             |
| Fim do suporte do servidor<br/>    | Windows Server 2008<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Media Foundation](media-foundation-functions.md)
</dt> <dt>

[Manipuladores de esquema e manipuladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Resolvedor de origem](source-resolver.md)
</dt> </dl>

 

 
