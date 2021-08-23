---
description: O método IsOwned da classe Win32 \_ Tpm indica se o dispositivo tem um proprietário. Esse valor é alterado pelo método TakeOwnership.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Método IsOwned da classe Win32_Tpm classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 01686f9b93e4dd952ce42b43d58aed9684457fb9dedeb524cea8859e0f44ba4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797106"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a>Método IsOwned da classe Win32 \_ Tpm

O **método IsOwned** da classe [**Win32 \_ Tpm**](win32-tpm.md) indica se o dispositivo tem um proprietário. Esse valor é alterado pelo [**método TakeOwnership.**](takeownership-win32-tpm.md)

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsOwned* \[ out\]
</dt> <dd>

Tipo: **booliana**

Se **for true,** o dispositivo terá um proprietário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Todos os erros do TPM, bem como erros específicos dos Serviços Base do TPM, podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Valor/código de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                      |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
