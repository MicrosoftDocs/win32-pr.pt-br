---
description: Cria o subtipo especificado dentro do tipo especificado.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'Método IPStore:: CreateSubtype (Pstore. h)'
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
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751553"
---
# <a name="ipstorecreatesubtype-method"></a>Método IPStore:: CreateSubtype

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

*Chave* \[ no\]
</dt> <dd>

Especifica a área de armazenamento do provedor.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHAVE \_ do \_ usuário atual**</dt> <dt>0x00000000</dt> </dl>    | O armazenamento é mantido na seção usuário atual do registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ \_ \_ Computador local da chave**</dt> <dt>0x00000001</dt> </dl> | O armazenamento é mantido na seção máquina local do registro.<br/> |



 

</dd> <dt>

*pType* \[ no\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o tipo de dados do armazenamento.

</dd> <dt>

*pSubtype* \[ no\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o subtipo de dados do armazenamento.

</dd> <dt>

*pInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ TYPEINFO de PST**](pst-typeinfo.md) .

</dd> <dt>

*pRules* \[ no\]
</dt> <dd>

Um ponteiro para uma [**estrutura \_ ACCESSRULESET de PST**](pst-accessruleset.md) .

**Windows XP:** Esse parâmetro é ignorado.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Reservado deve ser definido como zero.

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

[**\_ACCESSRULESET PST**](pst-accessruleset.md)
</dt> <dt>

[**TYPEINFO de PST \_**](pst-typeinfo.md)
</dt> </dl>

 

 
