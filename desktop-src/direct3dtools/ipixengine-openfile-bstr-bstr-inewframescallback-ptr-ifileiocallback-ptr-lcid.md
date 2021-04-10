---
description: Abre um log de gráficos.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine:: OpenFile'
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
ms.openlocfilehash: d18b0ff4d6d2301c6d52d2bc855d48a3db124ccb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087545"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>Método IPixEngine:: OpenFile

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

*Nome do arquivo*   
Uma cadeia de caracteres COM que contém o nome do log de gráficos.

*registryBoot*   
Uma cadeia de caracteres COM que contém a raiz do registro. O mecanismo é exibido aqui para o DIA e outras chaves do registro.

*retornos*   
O endereço de uma função usada para notificar o host que novos quadros foram analisados.

*pFileIOCallback*   
O endereço de uma função usada para notificar o host de erros de e/s de arquivo durante a análise.

*uiLocale*   
A ID de localidade usada para apresentar mensagens de erro de acordo com as configurações de localidade.

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Consulte também

[**IPixEngine**](/windows/desktop/direct3dtools/ipixengine)

 

 
