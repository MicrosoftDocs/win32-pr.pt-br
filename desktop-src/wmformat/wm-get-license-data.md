---
title: Estrutura de WM_GET_LICENSE_DATA (Drmexternals. h)
description: A \_ estrutura de \_ dados obter licença do WM \_ contém informações sobre onde adquirir uma licença DRM.
ms.assetid: 7e8053d5-f3f5-4519-97f5-6dbd89982f3a
keywords:
- Formato de mídia do Windows de estrutura de WM_GET_LICENSE_DATA
topic_type:
- apiref
api_name:
- WM_GET_LICENSE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f53b6ddfd532710e712637c57785d8893d8f977807bfb45cac0fc787ccbf58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844470"
---
# <a name="wm_get_license_data-structure"></a>\_Estrutura de \_ dados obter licença do WM \_

A estrutura de **\_ \_ \_ dados obter licença do WM** contém informações sobre onde adquirir uma [*licença*](wmformat-glossary.md) [*DRM*](wmformat-glossary.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WMGetLicenseData {
  DWORD   dwSize;
  HRESULT hr;
  WCHAR   *wszURL;
  WCHAR   *wszLocalFilename;
  BYTE    *pbPostData;
  DWORD   dwPostDataSize;
} WM_GET_LICENSE_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwSize**
</dt> <dd>

**DWORD** que contém o tamanho da estrutura de **\_ \_ \_ dados obter licença do WM** , em bytes.

</dd> <dt>

**h**
</dt> <dd>

Código de retorno **HRESULT** .

</dd> <dt>

**wszURL**
</dt> <dd>

Cadeia de caracteres com terminação nula de caractere largo que contém a URL de aquisição de licença. Use essa cadeia de caracteres e a cadeia de caracteres **pbPostData** em aquisição de licença não silenciosa.

</dd> <dt>

**wszLocalFilename**
</dt> <dd>

Cadeia de caracteres com terminação nula de caractere largo que contém uma página HTML local que é gerada pelo componente DRM. Quando essa cadeia de caracteres é carregada em um navegador, ela redireciona automaticamente a solicitação HTTP para a URL de aquisição de licença, juntamente com os dados de postagem necessários. O uso desta URL local agora está preterido. A abordagem recomendada é usar as cadeias de caracteres **wszURL** e **pbPostData** .

</dd> <dt>

**pbPostData**
</dt> <dd>

Ponteiro para uma matriz de bytes que contém os dados a serem postados na URL de aquisição de licença. Você deve adicionar a seguinte cadeia de caracteres ao início da cadeia de caracteres **pbPostData** : "nonsilent = 1&desafio =". A cadeia de caracteres resultante deve ser acrescentada a **wszURL** quando você formar a solicitação HTTP.

</dd> <dt>

**dwPostDataSize**
</dt> <dd>

**DWORD** que indica o tamanho de **pbPostData** sem a cadeia de caracteres "unsilent = 1&desafio =" referenciada em **pbPostData**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura preenchida é retornada *no parâmetro de* número de bits do método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) se **WMT \_ status** for igual a **WMT \_ sem \_ direitos \_ ex** ou **WMT \_ adquirir \_ licença**. Para WMT \_ nenhum \_ direito de \_ eventos ex, o membro de **RH** será \_ licença NS e \_ \_ necessária, NS \_ e licença \_ \_ desatualizado ou \_ \_ \_ direitos incorretos de licença NS e \_ . Qualquer um desses erros indica que uma nova licença deve ser adquirida navegando até a URL no membro **wszURL** .

Para eventos de licença de aquisição de WMT \_ \_ , o membro de **RH** passará a macro com êxito se uma licença tiver sido adquirida com êxito. Se esse evento for recebido após uma tentativa de aquisição silenciosa e o **HR** for igual a \_ licença NS e \_ DRM \_ \_ não adquirida, isso indica que apenas a aquisição não silenciosa é suportada pelo servidor de licença para esta licença.

O aplicativo de exemplo AudioPlayer demonstra como usar corretamente as informações retornadas nesta estrutura.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Versão<br/>                  | Windows SDK do Media Format 7 ou versões posteriores do SDK<br/>                       |
| Cabeçalho<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





