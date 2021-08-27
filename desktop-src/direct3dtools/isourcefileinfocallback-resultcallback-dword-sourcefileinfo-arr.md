---
description: Uma função de retorno de chamada usada para notificar o host de informações sobre arquivos de origem associados à callstack.
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método ISourceFileInfoCallback::ResultCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a50dba592f67a4628501d6a9a92bfe379daed09
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626342"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>Método ISourceFileInfoCallback::ResultCallback

Uma função de retorno de chamada usada para notificar o host de informações sobre arquivos de origem associados à callstack.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a>Parâmetros

*Contar*   
O número de arquivos de origem retornados.

*count0 \_ sourceFileInfoBuffer*   
Os arquivos de origem.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**ISourceFileInfoCallback**](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
