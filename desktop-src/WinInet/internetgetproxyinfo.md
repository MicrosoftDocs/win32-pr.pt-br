---
title: Função InternetGetProxyInfo
description: Recupera dados de proxy para acessar os recursos especificados.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- Função InternetGetProxyInfo WinINet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef441754fd5de09e3792d9269f05d96ecc08aa23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369631"
---
# <a name="internetgetproxyinfo-function"></a>Função InternetGetProxyInfo

> [!NOTE]
> Esta função é preterida. Para obter suporte a AutoProxy, use o protocolo WinHTTP (HTTP Services) versão 5,1 em vez disso. Para obter mais informações, consulte [WinHTTP AutoProxy support](../winhttp/winhttp-autoproxy-support.md).

Recupera dados de proxy para acessar os recursos especificados. Essa função só pode ser chamada por meio da vinculação dinâmica a "JSProxy.dll".

## <a name="syntax"></a>Sintaxe

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszUrl* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a URL do recurso de HTTP de destino.

</dd> <dt>

*dwUrlLength* \[ no\]
</dt> <dd>

O tamanho, em bytes, da URL apontada por *lpszUrl*.

</dd> <dt>

*lpszUrlHostName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do host da URL de destino.

</dd> <dt>

*dwUrlHostNameLength* \[ no\]
</dt> <dd>

O tamanho, em bytes, do nome do host apontado por *lpszUrlHostName*.

</dd> <dt>

*lplpszProxyHostName* \[ fora\]
</dt> <dd>

Um ponteiro para o endereço de um buffer que recebe a URL do proxy a ser usada em uma solicitação HTTP para o recurso especificado. O aplicativo é responsável por liberar essa cadeia de caracteres.

</dd> <dt>

*lpdwProxyHostNameLength* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho, em bytes, da cadeia de caracteres retornada no buffer *lplpszProxyHostName* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário. Para obter dados de erro estendidos, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Para chamar **InternetGetProxyInfo**, você deve vincular-se dinamicamente a ele usando o tipo de ponteiro de função definido **pfnInternetGetProxyInfo**. O trecho de código abaixo mostra como declarar uma instância desse tipo de ponteiro de função e, em seguida, inicializá-lo e chamá-lo.

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

Como todos os outros aspectos da API do WinINet, essa função não pode ser chamada com segurança de em DllMain ou os construtores e destruidores de objetos globais.

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>JSProxy.dll</dt> </dl> |

## <a name="see-also"></a>Confira também

[**InternetInitializeAutoProxyDll**](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))

[**DetectAutoProxyUrl**](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
