---
description: Define os dados para o valor de uma chave do Registro especificada em um hive do registro offline.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Função ORSetValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752370"
---
# <a name="orsetvalue-function"></a>Função ORSetValue

Define os dados para o valor de uma chave do Registro especificada em um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*lpValueName* \[ em, opcional\]
</dt> <dd>

O nome do valor a ser definido. Se um valor com esse nome ainda não estiver presente na chave, a função o adicionará à chave.

Se *lpValueName* for **nulo** ou uma cadeia de caracteres vazia, "", a função definirá o tipo e os dados para o valor padrão ou não nomeado da chave.

Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).

As chaves do registro não têm valores padrão, mas podem ter um valor não nomeado, que pode ser de qualquer tipo.

</dd> <dt>

*dwType* \[ no\]
</dt> <dd>

O tipo de dados apontado pelo parâmetro *lpData* . Para obter uma lista dos tipos possíveis, consulte [tipos de valor do registro](../sysinfo/registry-value-types.md).

</dd> <dt>

*lpData* \[ em, opcional\]
</dt> <dd>

Os dados a serem armazenados.

Para tipos baseados em cadeia de caracteres, como REG \_ sz, a cadeia de caracteres deve ser terminada em nulo. Para o \_ tipo de dados reg multi \_ sz, a cadeia de caracteres deve ser terminada com dois caracteres nulos.

</dd> <dt>

*cbData* \[ no\]
</dt> <dd>

O tamanho das informações apontadas pelo parâmetro *lpData* , em bytes. Se os dados forem do tipo REG \_ sz, Reg \_ Expand \_ sz ou reg \_ multi \_ sz, *cbData* deverá incluir o tamanho do caractere ou dos caracteres nulos de terminação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

## <a name="remarks"></a>Comentários

Os tamanhos de valor são limitados pela memória disponível. Valores longos (mais de 2048 bytes) devem ser armazenados como arquivos com os nomes de arquivo armazenados no registro. Isso ajuda o registro a ser executado com eficiência. Elementos de aplicativo, como ícones, bitmaps e arquivos executáveis, devem ser armazenados como arquivos e não podem ser colocados no registro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
