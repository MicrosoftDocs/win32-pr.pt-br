---
description: Abre um log de gráficos.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IPixEngine::OpenFile
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f6b2e34258221353baf541ddf76df205472f731
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624342"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>Método IPixEngine::OpenFile

Abre um log de gráficos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a>Parâmetros

*Filename*   
Uma cadeia de caracteres COM que contém o nome do log de gráficos.

*registryBoot*   
Uma cadeia de caracteres COM que contém a raiz do Registro. O mecanismo procura aqui por DIA e outras chaves do Registro.

*Retornos*   
O endereço de uma função usada para notificar o host de que novos quadros foram analisados.

*pFileIOCallback*   
O endereço de uma função usada para notificar o host de erros de E/S de arquivo durante a análise.

*uiLocale*   
A ID de localidade usada para apresentar mensagens de erro de acordo com as configurações de localidade.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPixEngine**](/windows/desktop/direct3dtools/ipixengine)

 

 
