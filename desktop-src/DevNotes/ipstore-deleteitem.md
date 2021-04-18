---
description: Exclui o item especificado do armazenamento protegido.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: 'IPStore: método eleteItem de:D (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749508"
---
# <a name="ipstoredeleteitem-method"></a>IPStore: método eleteItem de:D

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Exclui o item especificado do armazenamento protegido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
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

Um ponteiro para um **GUID** que identifica o tipo de dados do item a ser excluído.

</dd> <dt>

*pItemSubType* \[ no\]
</dt> <dd>

Um **GUID** que indica o subtipo de item a ser excluído.

</dd> <dt>

*szItemName* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que contém o nome do item a ser excluído.

</dd> <dt>

*pPromptInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma [**estrutura \_ PROMPTINFO de PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Especifica a interface do usuário e os comportamentos de segurança para a operação de exclusão.



| Valor                                                                                                                                                                                                                                             | Significado                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ NENHUMA \_ \_ migração de interface do usuário**</dt> <dt>0x00000010</dt> </dl> | Não mostrar interface do usuário, a menos que uma senha personalizada seja necessária.<br/> |



 

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

 

 
