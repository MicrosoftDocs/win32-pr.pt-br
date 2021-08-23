---
description: Grava um item de dados no armazenamento protegido.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: Método IPStore::WriteItem (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d8af896d2aca8ae218ba06f94cb0e2ef5f86fc4122acf3463356f5fea3dafd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955885"
---
# <a name="ipstorewriteitem-method"></a>Método IPStore::WriteItem

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Grava um item de dados no armazenamento protegido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ Em\]
</dt> <dd>

A área de armazenamento do provedor.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHAVE \_ ATUAL \_ DO USUÁRIO**</dt> <dt>0X00000000</dt> </dl>    | O armazenamento é mantido na seção de usuário atual do Registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHAVE \_ DO \_ COMPUTADOR LOCAL**</dt> <dt>0X00000001</dt> </dl> | O armazenamento é mantido na seção computador local do Registro.<br/> |



 

</dd> <dt>

*pItemType* \[ Em\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o tipo de dados do item de dados que está sendo gravado.

</dd> <dt>

*pItemSubtype* \[ Em\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o subtipo de dados do item de dados que está sendo gravado.

</dd> <dt>

*szItemName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome atribuído ao item de dados armazenados.

</dd> <dt>

*cbData* \[ out\]
</dt> <dd>

Um ponteiro para um **DWORD** que indica o tamanho do buffer que contém o item de dados armazenados.

</dd> <dt>

*ppbData* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que contém o item de dados que está sendo gravado.

</dd> <dt>

*pProomptInfo* \[ Em\]
</dt> <dd>

Ponteiro para uma [**estrutura PST \_ PROMPTINFO.**](pst-promptinfo.md)

</dd> <dt>

*dwDefaultConfirmationStyle* \[ Em\]
</dt> <dd>

O estilo de confirmação padrão.



| Valor                                                                                                                                                                                                                             | Significado                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**PST \_ CF \_ DEFAULT**</dt> <dt>0x00000000</dt> </dl> | Permite que o usuário escolha o estilo de confirmação. <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**PST \_ CF \_ NONE**</dt> <dt>0x00000001</dt> </dl>          | Força a criação silenciosa de item. <br/>                      |



 

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

A interface do usuário e os comportamentos de segurança para a operação de gravação.



| Valor                                                                                                                                                                                                                                                              | Significado                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**PST \_ SEM \_ SUBSTITUIR**</dt> <dt>0X00000002</dt> </dl>                            | Especifica que o item seja criado no armazenamento protegido. A substituição de um item existente não é permitido.<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ ITENS \_ IRRESTRITOS**</dt> <dt>0X00000004</dt> </dl> | Especifica que o fluxo de dados não é sesecure. Por padrão, as chamadas de item são seguras.<br/>                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um **valor HRESULT.** Um valor de **PST \_ E OK \_ indica** que a função foi bem-sucedida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**PST \_ PROMPTINFO**](pst-promptinfo.md)
</dt> </dl>

 

 
