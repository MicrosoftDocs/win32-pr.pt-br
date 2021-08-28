---
description: Cria o subtipo especificado dentro do tipo especificado.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: Método IPStore::CreateSubtype (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: da82d1edac78fab26f47be5bc333558355d04c3627342ece904a4005e9ebfa2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749986"
---
# <a name="ipstorecreatesubtype-method"></a>Método IPStore::CreateSubtype

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Cria o subtipo especificado dentro do tipo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSubtype(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ Em\]
</dt> <dd>

Especifica a área de armazenamento do provedor.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHAVE \_ ATUAL \_ DO USUÁRIO**</dt> <dt>0X00000000</dt> </dl>    | O armazenamento é mantido na seção de usuário atual do Registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHAVE \_ DO \_ COMPUTADOR LOCAL**</dt> <dt>0X00000001</dt> </dl> | O armazenamento é mantido na seção computador local do Registro.<br/> |



 

</dd> <dt>

*pType* \[ Em\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o tipo de dados do armazenamento.

</dd> <dt>

*pSubtype* \[ Em\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o subtipo de dados do armazenamento.

</dd> <dt>

*pInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura \_ TYPEINFO PST.**](pst-typeinfo.md)

</dd> <dt>

*pRules* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura PST \_ ACCESSRULESET.**](pst-accessruleset.md)

**Windows XP:** Esse parâmetro é ignorado.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Reservado; deve ser definido como zero.

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

[**PST \_ ACCESSRULESET**](pst-accessruleset.md)
</dt> <dt>

[**PST \_ TYPEINFO**](pst-typeinfo.md)
</dt> </dl>

 

 
