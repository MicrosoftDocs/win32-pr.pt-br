---
description: Indica a ação do usuário necessária para executar a operação de Trusted Platform Module presença física (TPM). Use o método SetPhysicalPresenceRequest para solicitar uma operação.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Método GetPhysicalPresenceTransition da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 939f29d923182d3e2b0b9237c49c2a5fc6ff8652d2361f867a7e95af48415654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906336"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>Método GetPhysicalPresenceTransition da classe Win32 \_ Tpm

O **método GetPhysicalPresenceTransition** da classe [**\_ Win32 Tpm**](win32-tpm.md) indica a ação do usuário necessária para executar a operação de presença física Trusted Platform Module (TPM). Use o [**método SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação. A ação de usuário necessária é definida para seu computador no momento da fabricação. Normalmente, uma reinicialização do computador é necessária.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Transição* \[ out\]
</dt> <dd>

Tipo: **uint32**

Um valor inteiro que especifica a transição necessária para executar uma operação de presença física do TPM.



| Valor                                                                        | Significado                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Nenhuma ação do usuário é necessária para executar uma operação de presença física do TPM.<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | Para executar uma operação de presença física do TPM, o usuário deve desligar o computador e, em seguida, a ligar novamente usando o botão de energia. O usuário deve estar fisicamente presente no computador para aceitar ou rejeitar a alteração quando solicitado pelo BIOS.<br/> |
| <dl> <dt>2</dt> </dl> | Para executar uma operação de presença física do TPM, o usuário deve reiniciar o computador usando uma reinicialização warm. O usuário deve estar fisicamente presente no computador para aceitar ou rejeitar a alteração quando solicitado pelo BIOS.<br/>                              |
| <dl> <dt>3</dt> </dl> | A ação de usuário necessária é desconhecida.<br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Todos os erros do TPM, bem como erros específicos dos Serviços Base do TPM, podem ser retornados.

A tabela a seguir lista alguns dos códigos de retorno comuns.



| Valor/código de retorno                                                                                                                                                                      | Descrição                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | O método foi bem-sucedido.<br/>                                                            |
| <dl> <dt>**TPM \_ E \_ PPI \_ ACPI \_ FAILURE**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Ocorreu uma falha de hardware. Consulte o fabricante do computador para obter mais informações.<br/> |



 

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

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
