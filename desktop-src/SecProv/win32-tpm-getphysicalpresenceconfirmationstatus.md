---
description: Indica se a confirmação de um usuário fisicamente presente é necessária para uma determinada operação de presença física.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: método Win32_Tpm::GetPhysicalPresenceConfirmationStatus
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
ms.openlocfilehash: 8e48fc7506b6b8ba8218d23bdeba75e960f2e3beca68c3d0a95b2aa4ea3c05e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890861"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>Método Win32 \_ Tpm::GetPhysicalPresenceConfirmationStatus

Indica se a confirmação de um usuário fisicamente presente é necessária para uma determinada operação de presença física.

Esse método só é acessível por administradores locais.

## <a name="syntax"></a>Sintaxe


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Operação* \[ Em\]
</dt> <dd>

Um valor inteiro que especifica a operação TPM solicitada que requer presença física. Também há suporte para comandos específicos do fornecedor.

O *parâmetro Operation* pode consistir nos valores a seguir.



| Valor                                                                                                                               | Significado                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | Habilitar<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | Desabilitar<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | Ativar<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | Desativar<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | Limpar<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | Habilitar + Ativar<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | Desativar + Desabilitar<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | SetOwnerInstall \_ True<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | SetOwnerInstall \_ False<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | Habilitar + Ativar + SetOwnerInstall \_ True<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | SetOwnerInstall \_ False + Deactivate + Disable<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | Presença física adiadaunownedFieldUpgrade<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | Limpar + Habilitar + Ativar<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ False<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ True<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ False<br/>                          |
| <dl> <dt>18</dt> </dl>                                                       | SetNoPPIClear \_ True<br/>                           |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ False<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ True<br/>                     |
| <dl> <dt>21</dt> </dl>                                                       | Habilitar + Ativar + Limpar<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | Habilitar + Ativar + Limpar + Habilitar + Ativar<br/> |



 

</dd> <dt>

*ConfirmationStatus* \[ out\]
</dt> <dd>

Retorna o status de confirmação para o comando de presença física.

O *parâmetro ConfirmationStatus* pode consistir nos valores a seguir.



| Valor                                                                        | Significado                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Não implementado<br/>                                             |
| <dl> <dt>1</dt> </dl> | Somente BIOS.<br/>                                                  |
| <dl> <dt>2</dt> </dl> | Bloqueado para o sistema operacional pela configuração do BIOS.<br/> |
| <dl> <dt>3</dt> </dl> | Usuário permitido e fisicamente presente necessário.<br/>               |
| <dl> <dt>4</dt> </dl> | Usuário permitido e fisicamente presente não é necessário<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Todos os erros do TPM, bem como erros específicos dos [Serviços Base do TPM,](../tbs/tbs-return-codes.md) podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Valor/código de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
