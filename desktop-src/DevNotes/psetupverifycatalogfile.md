---
description: Verifica um único arquivo de catálogo usando a política de assinatura de código do sistema operacional padrão, como assinatura de driver.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: função pSetupVerifyCatalogFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747871"
---
# <a name="psetupverifycatalogfile-function"></a>função pSetupVerifyCatalogFile

\[Esta função não é mais suportada pela Microsoft. Para um arquivo INF (instalação do dispositivo), os desenvolvedores devem usar o **SetupVerifyInfFile**. Para validar um catálogo não baseado em INF, use **WinVerifyTrust**.\]

Verifica um único arquivo de catálogo usando a política de assinatura de código do sistema operacional padrão, como assinatura de driver.

## <a name="syntax"></a>Sintaxe


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CatalogFullPath* \[ no\]
</dt> <dd>

O caminho totalmente qualificado do arquivo de catálogo a ser verificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, ela retornará **\_ êxito de erro**; caso contrário, retornará o erro de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SetupVerifyInfFile**](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
