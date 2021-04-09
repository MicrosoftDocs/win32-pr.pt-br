---
title: Estrutura de WINBIO_IDENTITY (WinBio \_ Types. h)
description: Contém um valor de identificação associado a um modelo biométrico.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_IDENTITY
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
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085661"
---
# <a name="winbio_identity-structure"></a>\_Estrutura de identidade WINBIO

A estrutura de **\_ identidade WINBIO** contém um valor de identificação associado a um modelo biométrico.

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
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**\_tipo de ID WINBIO \_ \_ NULL**</dt> </dl>             | O modelo não tem nenhuma ID associada.<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**\_tipo de ID WINBIO \_ \_ curinga**</dt> </dl> | A estrutura corresponde a todas as identidades de modelo.<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**\_GUID do \_ tipo de ID de WINBIO \_**</dt> </dl>             | A estrutura contém um GUID associado ao modelo.<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**\_SID do \_ tipo de ID de WINBIO \_**</dt> </dl>                | A estrutura contém o SID da conta associado ao modelo.<br/> |



 

</dd> <dt>

**Valor**
</dt> <dd>

Uma União que pode conter um dos seguintes valores:

<dl> <dt>

**Nulo**
</dt> <dd>

Contém 1 se o membro do **tipo** for **WINBIO \_ ID \_ Type \_ NULL**.

</dd> <dt>

**Amplia**
</dt> <dd>

Contém 1 se o membro de **tipo** for um **tipo de \_ ID WINBIO \_ \_ curinga**.

</dd> <dt>

**TemplateGuid**
</dt> <dd>

Contém um valor de GUID de 128 bits que identifica o modelo se o membro de **tipo** for o **tipo de \_ ID WINBIO \_ \_ GUID**.

</dd> <dt>

**AccountSid**
</dt> <dd>

Uma estrutura que contém um SID de conta se o membro do **tipo** for **WINBIO \_ ID do \_ tipo \_ Sid**.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> </dl>

 

 





