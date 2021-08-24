---
description: Define sinalizadores de virtualização na chave do Registro aberta especificada em um hive do Registro offline.
ms.assetid: c625af35-8e14-4379-8d0a-6f5b65a1aebb
title: Função ORSetVirtualFlags (Offreg.h)
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
ms.openlocfilehash: 56ca40b273447c8669c162b8c2dba597f2b2ce98282d40e7b482d04032a5f95a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815436"
---
# <a name="orsetvirtualflags-function"></a>Função ORSetVirtualFlags

Define sinalizadores de virtualização na chave do Registro aberta especificada em um hive do Registro offline.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ORSetVirtualFlags(
  _In_ ORHKEY Handle,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Manipular* \[ Em\]
</dt> <dd>

Um handle para uma chave aberta do Registro em um hive de registro offline.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Esse parâmetro controla o comportamento do Registro quando uma operação Criar ou Abrir falha em uma chave em um hive virtualizado. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**REG \_ FALHA \_ SILENCIOSA DE \_ KEY \_ DONT**</dt> <dt>4</dt> </dl> | Se esse sinalizador for definido e uma operação Abrir falhar em uma chave para a qual a virtualização está habilitada, o Registro não tentará reabrir a chave. Se esse sinalizador estiver claro, o Registro tentará reabrir a chave com o acesso MÁXIMO \_ PERMITIDO.<br/>                                                                                    |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**REG \_ KEY \_ DONT \_ VIRTUALIZE**</dt> <dt>2</dt> </dl>     | Se esse sinalizador for definido e uma operação Criar Chave falhar porque o chamador não tem o direito KEY CREATE SUB KEY na chave pai, o Registro falhará na \_ \_ operação \_ Criar. Se esse sinalizador estiver claro, o Registro tentará criar a chave no armazenamento virtual. O chamador deve ter a tecla KEY \_ READ à direita na chave pai.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**REG \_ SINALIZADOR \_ DE RECURSE \_ DE CHAVE**</dt> <dt>8</dt> </dl>              | Se esse sinalizador for definido, os sinalizadores de virtualização do Registro serão propagados da chave pai. Se esse sinalizador estiver claro, os sinalizadores de virtualização do Registro não serão propagados.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro não zero definido em Winerror.h. Você pode usar a [função FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com o sinalizador FORMAT MESSAGE FROM SYSTEM para obter \_ uma \_ \_ descrição genérica do erro.

## <a name="remarks"></a>Comentários

A virtualização do Registro é uma tecnologia de compatibilidade de aplicativo provisório que permite que as operações de gravação do Registro que têm impacto global sejam redirecionadas para locais por usuário. Esse redirecionamento é transparente para aplicativos que lêem ou escrevem no Registro.

A virtualização do Registro tem suporte a partir do Windows Vista. No entanto, a Microsoft pretende removê-lo de versões futuras do sistema operacional Windows à medida que mais aplicativos são compatíveis com o Windows Vista. Portanto, os aplicativos não devem depender do comportamento da virtualização do Registro no sistema.

A virtualização do Registro está habilitada somente para o seguinte:

-   Processos interativos de 32 bits
-   Chaves no **HKEY \_ LOCAL MACHINE \_ \\ Software**
-   Chaves nas que um administrador pode gravar

Para obter mais informações, consulte [Virtualização do Registro](../sysinfo/registry-virtualization.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Windows Biblioteca de Registro offline versão 1.0 ou posterior<br/>                      |
| Cabeçalho<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORGetVirtualFlags**](orgetvirtualflags.md)
</dt> <dt>

[Virtualização do Registro](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
