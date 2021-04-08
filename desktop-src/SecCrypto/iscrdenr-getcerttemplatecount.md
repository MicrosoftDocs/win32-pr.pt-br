---
description: Recupera o número de modelos de certificado.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'Método ISCrdEnr:: getCertTemplateCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836984"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a>Método ISCrdEnr:: getCertTemplateCount

O método **getCertTemplateCount** recupera o número de modelos de certificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Um valor que determina se o modelo é para certificados de usuário ou computador. Se esse valor for SCARTAR \_ registrar \_ \_ \_ o modelo de certificado do usuário (definido como 1), a contagem retornada será para modelos de certificado do usuário. Se esse valor for SCARTAR \_ registrar \_ \_ \_ o modelo de certificado de máquina (definido como 2), a contagem retornada será para modelos de certificado de máquina.

</dd> <dt>

*pdwCertTemplateCount* \[ fora\]
</dt> <dd>

Um ponteiro para um **longo** que retorna o número de modelos de certificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="c"></a>C++

Se o método for bem sucedido, o método retornará S \_ OK.

Se o método falhar, ele retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Um valor **longo** que representa o número de modelos de certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




