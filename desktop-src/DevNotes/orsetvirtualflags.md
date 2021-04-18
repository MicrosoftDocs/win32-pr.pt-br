---
description: Define os sinalizadores de virtualização na chave do registro aberta especificada em um hive do registro offline.
ms.assetid: c625af35-8e14-4379-8d0a-6f5b65a1aebb
title: Função ORSetVirtualFlags (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: f694d69684a474cfa6d4f6c33c6d8cab7072f605
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755754"
---
# <a name="orsetvirtualflags-function"></a>Função ORSetVirtualFlags

Define os sinalizadores de virtualização na chave do registro aberta especificada em um hive do registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORSetVirtualFlags(
  _In_ ORHKEY Handle,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificador* \[ do no\]
</dt> <dd>

Um identificador para uma chave do registro aberta em um hive do registro offline.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro controla o comportamento do registro quando uma operação de criação ou abertura falha em uma chave em um Hive virtualizado. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**Reg \_ CHAVE \_ não \_ silenciosa com \_ falha**</dt> <dt>4</dt> </dl> | Se esse sinalizador for definido e uma operação de abertura falhar em uma chave para a qual a virtualização está habilitada, o registro não tentará reabrir a chave. Se esse sinalizador estiver claro, o registro tentará reabrir a chave com o máximo \_ permitido de acesso.<br/>                                                                                    |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**Reg \_ A chave não \_ \_ virtualiza**</dt> <dt>2</dt> </dl>     | Se esse sinalizador for definido e uma operação de criação de chave falhar porque o chamador não tem a chave \_ Create \_ sub \_ Key diretamente na chave pai, o registro falhará na operação de criação. Se esse sinalizador for claro, o registro tentará criar a chave no repositório virtual. O chamador deve ter o direito de leitura de chave \_ na chave pai.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**Reg \_ \_ \_ Sinalizador de recursão de chave**</dt> <dt>8</dt> </dl>              | Se esse sinalizador for definido, os sinalizadores de virtualização do registro serão propagados da chave pai. Se esse sinalizador for claro, os sinalizadores de virtualização do registro não serão propagados.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h. Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.

## <a name="remarks"></a>Comentários

A virtualização do registro é uma tecnologia de compatibilidade de aplicativos provisória que permite que as operações de gravação do registro que têm impacto global sejam redirecionadas para locais por usuário. Esse redirecionamento é transparente para os aplicativos que lêem ou gravam no registro.

A virtualização do registro tem suporte a partir do Windows Vista. No entanto, a Microsoft pretende removê-la de versões futuras do sistema operacional Windows à medida que mais aplicativos são tornados compatíveis com o Windows Vista. Portanto, os aplicativos não devem depender do comportamento da virtualização do registro no sistema.

A virtualização do registro é habilitada apenas para o seguinte:

-   processos interativos de 32 bits
-   Chaves em **HKEY \_ local \_ Machine \\ software**
-   Chaves que um administrador pode gravar

Para obter mais informações, consulte [virtualização de registro](../sysinfo/registry-virtualization.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORGetVirtualFlags**](orgetvirtualflags.md)
</dt> <dt>

[Virtualização do registro](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
