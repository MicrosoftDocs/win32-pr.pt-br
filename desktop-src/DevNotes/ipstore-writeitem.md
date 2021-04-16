---
description: Grava um item de dados no armazenamento protegido.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'Método IPStore:: WriteItem (Pstore. h)'
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
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752597"
---
# <a name="ipstorewriteitem-method"></a>Método IPStore:: WriteItem

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

*Chave* \[ no\]
</dt> <dd>

A área de armazenamento do provedor.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt> </dl>    | O armazenamento é mantido na seção usuário atual do registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt> </dl> | O armazenamento é mantido na seção máquina local do registro.<br/> |



 

</dd> <dt>

*pItemType* \[ no\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o tipo de dados do item de dados que está sendo gravado.

</dd> <dt>

*pItemSubtype* \[ no\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o subtipo de dados do item de dados que está sendo gravado.

</dd> <dt>

*szItemName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome atribuído ao item de dados armazenado.

</dd> <dt>

*cbData* \[ fora\]
</dt> <dd>

Um ponteiro para um **DWORD** que indica o tamanho do buffer que contém o item de dados armazenado.

</dd> <dt>

*ppbData* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que contém o item de dados que está sendo gravado.

</dd> <dt>

*pProomptInfo* \[ no\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ PROMPTINFO de PST**](pst-promptinfo.md) .

</dd> <dt>

*dwDefaultConfirmationStyle* \[ no\]
</dt> <dd>

O estilo de confirmação padrão.



| Valor                                                                                                                                                                                                                             | Significado                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**PST \_ \_Padrão de CF**</dt> <dt>0x00000000</dt> </dl> | Permite que o usuário escolha o estilo de confirmação. <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**PST \_ CF \_ nenhum**</dt> <dt>0x00000001</dt> </dl>          | Força a criação de itens silenciosos. <br/>                      |



 

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

A interface do usuário e os comportamentos de segurança para a operação de gravação.



| Valor                                                                                                                                                                                                                                                              | Significado                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**PST \_ Não \_ substituir**</dt> <dt>0x00000002</dt> </dl>                            | Especifica que o item seja criado no armazenamento protegido. A substituição de um item existente não é permitida.<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ \_Dados não restritos**</dt> <dt>0x00000004</dt> </dl> | Especifica que o fluxo de dados não é seguro. Por padrão, as chamadas de item são seguras.<br/>                         |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um valor **HRESULT** . Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**\_PROMPTINFO PST**](pst-promptinfo.md)
</dt> </dl>

 

 
