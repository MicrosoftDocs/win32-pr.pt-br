---
description: Recupera um valor que determina se o código dinâmico especificado na memória ou em disco do .NET CRL é confiável pela política de proteção do dispositivo.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Função WldpQueryDynamicCodeTrust (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500904"
---
# <a name="wldpquerydynamiccodetrust-function"></a>Função WldpQueryDynamicCodeTrust

Recupera um valor que determina se o código dinâmico especificado na memória ou em disco do .NET CRL é confiável pela política de proteção do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fileHandle* 
</dt> <dd>

Manipule o arquivo de código dinâmico em disco para verificar. Se *fileHandle* for não **nulo**, *baseImage* deverá ser **nulo**.

</dd> <dt>

*baseImage* 
</dt> <dd>

Ponteiro para o arquivo PE na memória a ser verificado. Se *baseImage* for não **nulo**, *fileHandle* deverá ser **nulo**.

</dd> <dt>

*ImageSize* 
</dt> <dd>

Quando *baseImage* é não **nulo**, indica o tamanho do buffer para o qual o *baseImage* aponta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




