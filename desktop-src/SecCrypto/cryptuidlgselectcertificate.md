---
description: Exibe uma caixa de diálogo que permite que um usuário selecione um certificado.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: Função CryptUIDlgSelectCertificate
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: fb37eb664841331ce3f37e9ce37ca3ab9e5c0f92c254cff0896c6c682a9f2872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768159"
---
# <a name="cryptuidlgselectcertificate-function"></a>Função CryptUIDlgSelectCertificate

A função **CryptUIDlgSelectCertificate** exibe uma caixa de diálogo que permite que um usuário selecione um certificado.

## <a name="syntax"></a>Sintaxe


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PCSC* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ struct CRYPTUI SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) que contém informações sobre a caixa de diálogo a ser exibida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um ponteiro para uma estrutura de [**\_ contexto de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) que representa o certificado selecionado pelo usuário. Quando você terminar de usar esse certificado, deverá passar esse ponteiro para a função [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) para diminuir a contagem de referência do contexto do certificado.

Se o membro **dwFlags** da estrutura *PCSC* não contiver o sinalizador **CRYPTUI \_ SELECTCERT \_ MultiSelect** , um valor de retorno de **NULL** significa que o usuário fechou a caixa de diálogo sem selecionar um certificado.

Se o membro **dwFlags** da estrutura *PCSC* contiver o sinalizador **CRYPTUI \_ SELECTCERT \_ MultiSelect** , essa função sempre retornará **NULL**. Os certificados selecionados estarão contidos no repositório de certificados que é representado pelo membro **hSelectedCertStore** de *PCSC*. Se o número de certificados no repositório for o mesmo antes e depois de chamar **CryptUIDlgSelectCertificate**, o usuário fechou a caixa de diálogo sem selecionar nenhum certificado.

## <a name="remarks"></a>Comentários

Se o membro **dwFlags** da estrutura [**de \_ \_ struct CRYPTUI SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) for definido como **CRYPTUI \_ SELECTCERT \_ Legacy**, a caixa de diálogo herdada será exibida. Caso contrário, a caixa de diálogo de seleção de certificado atual será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos da área de trabalho do Windows XP\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                              |
| Fim do suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                       |
| Biblioteca<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>            |
| Nomes Unicode e ANSI<br/>   | **CryptUIDlgSelectCertificateW** (Unicode) e **CryptUIDlgSelectCertificateA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CRYPTUI \_ SELECTCERTIFICATE \_ struct**](cryptui-selectcertificate-struct.md)
</dt> </dl>






