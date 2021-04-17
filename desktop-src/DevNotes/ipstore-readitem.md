---
description: Lê o item de dados especificado do armazenamento protegido.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'Método IPStore:: ReadItem (Pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755279"
---
# <a name="ipstorereaditem-method"></a>Método IPStore:: ReadItem

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Lê o item de dados especificado do armazenamento protegido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
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

Um ponteiro para um GUID que identifica o tipo de dados do item a ser lido.

</dd> <dt>

*pItemSubtype* \[ no\]
</dt> <dd>

Um ponteiro para um GUID que identifica o subtipo de dados do item a ser lido.

</dd> <dt>

*szItemName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome atribuído ao item de dados armazenado.

</dd> <dt>

*cbData* \[ no\]
</dt> <dd>

Um **DWORD** que indica o tamanho do buffer que contém o item de dados armazenado.

</dd> <dt>

*pbData* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém o item de dados armazenado.

</dd> <dt>

*pPromptInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma [**estrutura \_ PROMPTINFO de PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Especifica a interface do usuário e os comportamentos de segurança para a operação de leitura.

Os valores de sinalizador podem ser combinados com um OR lógico.



| Valor                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**PST \_ \_Dados não restritos**</dt> <dt>0x00000004</dt> </dl> | Especifica que o fluxo de dados não é seguro. Por padrão, as chamadas de item são seguras.<br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <dt>**PST \_ 0x00000008 de \_ consulta de prompt**</dt> <dt></dt> </dl>                            | Especifica que a confirmação será retornada após o êxito. Se a interface do usuário estiver habilitada, um sucesso do **PST \_ E \_ OK** será retornado. Se a interface do usuário não estiver habilitada, um valor de **PST \_ E \_ item \_ existente** será retornado.<br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**PST \_ NENHUMA \_ \_ migração de interface do usuário**</dt> <dt>0x00000010</dt> </dl>                  | Não mostrar interface do usuário, a menos que uma senha personalizada seja necessária.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um valor **HRESULT** . Um valor de **PST \_ E \_ OK** indica que a função foi bem-sucedida.

## <a name="remarks"></a>Comentários

Se o **ReadItem** for concluído com êxito, o aplicativo será responsável por liberar o buffer de dados retornado usando a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .

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

 

 
