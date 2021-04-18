---
description: Indica a ação do usuário necessária para executar a operação de presença física do Trusted Platform Module (TPM). Use o método SetPhysicalPresenceRequest para solicitar uma operação.
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
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758152"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a>Método GetPhysicalPresenceTransition da classe Win32 \_ TPM

O método **GetPhysicalPresenceTransition** da classe [**Win32 \_ TPM**](win32-tpm.md) indica a ação do usuário necessária para executar a operação de presença física do Trusted Platform Module (TPM). Use o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação. A ação do usuário necessária está definida para seu computador no momento da fabricação. Normalmente, é necessária uma reinicialização do computador.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Transição* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Um valor inteiro que especifica a transição necessária para executar uma operação de presença física de TPM.



| Valor                                                                        | Significado                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Nenhuma ação do usuário é necessária para executar uma operação de presença física do TPM.<br/>                                                                                                                                                                              |
| <dl> <dt>1</dt> </dl> | Para executar uma operação de presença física do TPM, o usuário deve desligar o computador e ligá-lo novamente usando o botão de energia. O usuário deve estar fisicamente presente no computador para aceitar ou rejeitar a alteração quando solicitado pelo BIOS.<br/> |
| <dl> <dt>2</dt> </dl> | Para executar uma operação de presença física de TPM, o usuário deve reiniciar o computador usando uma reinicialização a quente. O usuário deve estar fisicamente presente no computador para aceitar ou rejeitar a alteração quando solicitado pelo BIOS.<br/>                              |
| <dl> <dt>3</dt> </dl> | A ação do usuário necessária é desconhecida.<br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

A tabela a seguir lista alguns dos códigos de retorno comuns.



| Código/valor de retorno                                                                                                                                                                      | Descrição                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | O método foi bem-sucedido.<br/>                                                            |
| <dl> <dt>**TPM \_ \_Falha de \_ ACPI \_ PPI**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Ocorreu uma falha de hardware. Consulte o fabricante do seu computador para obter mais informações.<br/> |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                      |
| Namespace<br/>                | \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
