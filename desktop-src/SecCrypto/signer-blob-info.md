---
description: Especifica um BLOB a assinar.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: Estrutura de SIGNER_BLOB_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a865a65b5fd9a1ec658dcc86b1eb2b3dd255804308f04bebf4fffdb0650d71e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898923"
---
# <a name="signer_blob_info-structure"></a>Estrutura de informações de \_ blob do assinante \_

\[A estrutura de **\_ \_ informações de blob do assinante** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

A estrutura de **\_ \_ informações de blob do assinante** especifica um [*blob*](../secgloss/b-gly.md) a ser assinado.

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho, em bytes, da estrutura.

</dd> <dt>

**pGuidSubject**
</dt> <dd>

Um ponteiro para um **GUID** que especifica o pacote de interface de entidade (SIP) a ser carregado.

</dd> <dt>

**cbBlob**
</dt> <dd>

O tamanho, em bytes, do BLOB a ser assinado.

</dd> <dt>

**pbBlob**
</dt> <dd>

Um ponteiro para o BLOB a ser assinado.

</dd> <dt>

**pwszDisplayName**
</dt> <dd>

O nome de exibição do BLOB. Esse membro pode ser definido como **nulo**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações de assunto do assinante \_**](signer-subject-info.md)
</dt> </dl>

 

 
