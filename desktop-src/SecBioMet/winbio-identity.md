---
title: WINBIO_IDENTITY estrutura (Tipos \_ winbio.h)
description: Contém um valor de identificação associado a um modelo biométrico.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- WINBIO_IDENTITY estrutura Windows API do Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677a341386bcc937061798f406397028c23c10b65989480da975a9fdf81a3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910114"
---
# <a name="winbio_identity-structure"></a>Estrutura WINBIO \_ IDENTITY

A **estrutura WINBIO \_ IDENTITY** contém um valor de identificação associado a um modelo biométrico.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

Especifica o formato das informações de identidade contidas nesta estrutura. Esse valor pode ser um dos seguintes:



| Valor                                                                                                                                                                                         | Significado                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**TIPO \_ DE ID \_ WINBIO \_ NULL**</dt> </dl>             | O modelo não tem nenhuma ID associada.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**CURINGA DE \_ TIPO DE ID \_ \_ WINBIO**</dt> </dl> | A estrutura corresponde a todas as identidades de modelo.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**GUID DE \_ TIPO DE ID \_ DO WINBIO \_**</dt> </dl>             | A estrutura contém um GUID associado ao modelo.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**SID DE \_ TIPO DE ID \_ \_ DO WINBIO**</dt> </dl>                | A estrutura contém o SID da conta associado ao modelo.<br/> |



 

</dd> <dt>

**Valor**
</dt> <dd>

Uma união que pode conter um dos seguintes valores:

<dl> <dt>

**Nulo**
</dt> <dd>

Conterá 1 se **o membro Type** for **WINBIO \_ ID TYPE \_ \_ NULL.**

</dd> <dt>

**Curinga**
</dt> <dd>

Conterá 1 se **o membro Type** for **WINBIO \_ ID TYPE \_ \_ WILDCARD**.

</dd> <dt>

**TemplateGuid**
</dt> <dd>

Contém um valor guid de 128 bits que identifica o modelo se o membro **Type** for **WINBIO \_ ID \_ TYPE \_ GUID**.

</dd> <dt>

**AccountSid**
</dt> <dd>

Uma estrutura que contém um SID de conta se **o membro Type** for **WINBIO \_ ID TYPE \_ \_ SID.**

<dl> <dt>

**Tamanho**
</dt> <dd>

O número de caracteres no SID.

</dd> <dt>

**Dados**
</dt> <dd>

Uma matriz de caracteres não assinados que contêm o SID. O tamanho máximo atual da matriz é de 68 caracteres.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada nas seguintes funções:

-   [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> </dl>

 

 





