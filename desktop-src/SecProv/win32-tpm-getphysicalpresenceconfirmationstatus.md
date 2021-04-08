---
description: Indica se a confirmação de um usuário fisicamente presente é necessária para uma determinada operação de presença física.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Método Win32_Tpm:: GetPhysicalPresenceConfirmationStatus'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922103"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>\_Método TPM:: GetPhysicalPresenceConfirmationStatus do Win32

Indica se a confirmação de um usuário fisicamente presente é necessária para uma determinada operação de presença física.

Esse método só pode ser acessado por administradores locais.

## <a name="syntax"></a>Sintaxe


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Operação* \[ do no\]
</dt> <dd>

Um valor inteiro que especifica a operação de TPM solicitada que requer a presença física. Também há suporte para comandos específicos do fornecedor.

O parâmetro *Operation* pode consistir nos valores a seguir.



| Valor                                                                                                                               | Significado                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | Habilitar<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | Desabilitar<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | Ativar<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | Desativar<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | Limpar<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | Habilitar + ativar<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | Desativar + desabilitar<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | SetOwnerInstall \_ true<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | SetOwnerInstall \_ false<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | Habilitar + ativar + SetOwnerInstall \_ verdadeiro<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | SetOwnerInstall \_ false + desativar + desabilitar<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | PresenceunownedFieldUpgrade físico adiado<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | Limpar + habilitar + ativar<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ false<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ true<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ false<br/>                          |
| <dl> <dt>anos</dt> </dl>                                                       | SetNoPPIClear \_ true<br/>                           |
| <dl> <dt>aprimora</dt> </dl>                                                       | SetNoPPIMaintenance \_ false<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ true<br/>                     |
| <dl> <dt>Abril</dt> </dl>                                                       | Habilitar + ativar + limpar<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | Habilitar + ativar + limpar + habilitar + ativar<br/> |



 

</dd> <dt>

*ConfirmationStatus* \[ fora\]
</dt> <dd>

Retorna o status de confirmação para o comando de presença física.

O parâmetro *ConfirmationStatus* pode consistir nos valores a seguir.



| Valor                                                                        | Significado                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Não implementado<br/>                                             |
| <dl> <dt>1</dt> </dl> | Somente BIOS.<br/>                                                  |
| <dl> <dt>2</dt> </dl> | Bloqueado para o sistema operacional pela configuração do BIOS.<br/> |
| <dl> <dt>3</dt> </dl> | Usuário permitido e fisicamente presente necessário.<br/>               |
| <dl> <dt>4</dt> </dl> | Usuário permitido e fisicamente presente não é necessário<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
