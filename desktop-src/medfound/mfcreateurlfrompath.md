---
description: Converte um caminho do Microsoft MS-DOS em uma URL canônica.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: Função MFCreateURLFromPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793684"
---
# <a name="mfcreateurlfrompath-function"></a>Função MFCreateURLFromPath

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro. Em vez disso, os aplicativos devem chamar [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]

Converte um caminho do Microsoft MS-DOS em uma URL canônica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszFilePath* \[ em, opcional\]
</dt> <dd>

Uma cadeia de caracteres terminada em nulo que contém o caminho. O comprimento máximo da cadeia de caracteres é o **\_ \_ \_ comprimento máximo da URL da Internet**.

</dd> <dt>

*ppwszFileURL* \[ fora\]
</dt> <dd>

Recebe uma cadeia de caracteres terminada em nulo que contém a URL. O chamador deve liberar a cadeia de caracteres chamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                             | Description                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | A cadeia de caracteres fornecida no parâmetro *pwszFilePath* já está no formato de URL. Nesse caso, *pszFilePath* é simplesmente copiado para *ppszFileURL* sem modificação.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | A função foi bem-sucedida. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação associada. Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mfplat.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Media Foundation](media-foundation-functions.md)
</dt> </dl>

 

 
