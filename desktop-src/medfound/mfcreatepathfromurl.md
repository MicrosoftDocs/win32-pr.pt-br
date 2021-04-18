---
description: Converte uma URL de arquivo em um caminho do Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: Função MFCreatePathFromURL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780398"
---
# <a name="mfcreatepathfromurl-function"></a>Função MFCreatePathFromURL

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro. Em vez disso, os aplicativos devem chamar [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]

Converte uma URL de arquivo em um caminho do Microsoft MS-DOS.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszFileURL* \[ em, opcional\]
</dt> <dd>

Uma cadeia de caracteres terminada em nulo que contém a URL. O comprimento máximo da cadeia de caracteres é o **\_ \_ \_ comprimento máximo da URL da Internet**.

</dd> <dt>

*ppwszFilePath* \[ fora\]
</dt> <dd>

Recebe uma cadeia de caracteres terminada em nulo que contém a URL. O chamador deve liberar a cadeia de caracteres chamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Description                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A função foi bem-sucedida. <br/>                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento inválido. A cadeia de caracteres fornecida no parâmetro *pwszFileURL* não pode ser convertida em um caminho.<br/> |



 

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

 

 
