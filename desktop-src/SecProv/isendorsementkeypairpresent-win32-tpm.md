---
description: O método IsEndorsementKeyPairPresent da classe Win32 Tpm indica se o par de chaves de endosso \_ existe no dispositivo.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Método IsEndorsementKeyPairPresent da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: bcbc0c4877aae2db0e94d42838100720ee0ae0dcbdcc33f52cf70d2e23327e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004464"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a>Método IsEndorsementKeyPairPresent da classe \_ Win32 Tpm

O **método IsEndorsementKeyPairPresent** da classe [**\_ Win32 Tpm**](win32-tpm.md) indica se o par de chaves de endosso existe no dispositivo. O par de chaves de endosso é necessário antes que o dispositivo possa ser de propriedade. Esse par de chaves pode ser criado pelo [**método CreateEndorsementKeyPair.**](createendorsementkeypair-win32-tpm.md)

O dispositivo deve ser habilitado e ativado para que esse método seja bem-sucedido. Para habilitar e ativar um dispositivo sem proprietário, consulte o [**método SetPhysicalPresenceRequest.**](setphysicalpresencerequest-win32-tpm.md)

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsEndorsementKeyPairPresent* \[ out\]
</dt> <dd>

Tipo: **booliana**

Se **for true,** o par de chaves de endosso existirá no dispositivo.

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
</dt> <dt>

[**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
