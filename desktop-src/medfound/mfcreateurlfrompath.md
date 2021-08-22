---
description: Converte um caminho do Microsoft MS-DOS em uma URL canonizada.
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
ms.openlocfilehash: f9da3dd84d54bb514b7dda519db3de376b2ebb2bd2088d8fc8e18b4f2b848231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739244"
---
# <a name="mfcreateurlfrompath-function"></a>Função MFCreateURLFromPath

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro. Em vez disso, os aplicativos [devem chamar UrlCreateFromPath.](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha)\]

Converte um caminho do Microsoft MS-DOS em uma URL canonizada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszFilePath* \[ in, opcional\]
</dt> <dd>

Uma cadeia de caracteres terminada em nulo que contém o caminho. O comprimento máximo da cadeia de caracteres é **INTERNET \_ MAX URL \_ \_ LENGTH**.

</dd> <dt>

*ppwszFileURL* \[ out\]
</dt> <dd>

Recebe uma cadeia de caracteres terminada em nulo que contém a URL. O chamador deve liberar a cadeia de caracteres chamando [**CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | A cadeia de caracteres determinada no *parâmetro pwszFilePath* já está no formato de URL. Nesse caso, *pszFilePath é* simplesmente copiado para *ppszFileURL* sem modificação.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | A função foi bem-sucedida. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação associada. Para chamar essa função, você deve usar as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mfplat.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Mfplat.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation funções](media-foundation-functions.md)
</dt> </dl>

 

 
