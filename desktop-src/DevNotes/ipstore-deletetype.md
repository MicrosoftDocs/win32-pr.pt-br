---
description: Exclui um tipo especificado do banco de dados de armazenamento protegido.
ms.assetid: 5e3a08eb-e16b-4d9f-82be-241eb3137d17
title: Método IPStore::D eleteType (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 719918c980717784a680d462500295e916adf4f86d605db2c4f555cf77e10d67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667419"
---
# <a name="ipstoredeletetype-method"></a>Método IPStore::D eleteType

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Exclui um tipo especificado do banco de dados de armazenamento protegido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteType(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ Em\]
</dt> <dd>

Especifica se o tipo é local para o computador ou associado somente ao usuário que está criando.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**PST \_ CHAVE \_ ATUAL \_ DO USUÁRIO**</dt> <dt>0X00000000</dt> </dl>    | O armazenamento é mantido na seção de usuário atual do Registro.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**PST \_ CHAVE \_ DO COMPUTADOR LOCAL \_ 0X00000001**</dt> <dt></dt> </dl> | O armazenamento é mantido na seção computador local do Registro.<br/> |



 

</dd> <dt>

*pType* \[ Em\]
</dt> <dd>

Um ponteiro para um **GUID** que identifica o tipo de dados do armazenamento.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Reservado: deve ser definido como zero.

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
</dt> </dl>

 

 
