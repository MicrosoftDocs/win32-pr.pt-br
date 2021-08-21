---
description: Solicita uma operação TPM que requer presença física.
ms.assetid: e71eb6ab-b6ab-4586-8999-0a464f11047a
title: Método SetPhysicalPresenceRequest da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9c1b1e2760ed5015b6b682b94bd364e469edb4ed519adc371e2c348a0bf8c607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891351"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Método SetPhysicalPresenceRequest da classe \_ Win32 Tpm

O **método SetPhysicalPresenceRequest** da classe [**\_ Win32 Tpm**](win32-tpm.md) solicita uma operação TPM que requer presença física. Depois de usar esse método para enviar uma solicitação, aplique a próxima etapa indicada no [**método GetPhysicalPresenceTransition.**](getphysicalpresencetransition-win32-tpm.md) Por fim, use [**o método GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) para verificar se a operação foi bem-sucedida. Esse método suspenderá o BitLocker se a chamada puder fazer com que a recuperação do BitLocker seja necessária. O BitLocker será retomado automaticamente depois que o TPM tiver sido provisionado.

Essas etapas são necessárias porque as operações de presença física podem ser executados somente depois que o computador detectar o usuário fisicamente presente.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Solicitação* \[ Em\]
</dt> <dd>

Tipo: **uint32**

Um valor inteiro que especifica a operação TPM solicitada que requer presença física.



| Valor                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | Nenhuma solicitação.<br/> Use esse valor para limpar uma solicitação pendente.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | Habilita o TPM.<br/> Essa operação é invertida pela operação 2.<br/> Para obter mais informações, consulte os seguintes métodos relacionados que não envolvem a presença física: [**Enable**](enable-win32-tpm.md) e [**IsEnabled.**](isenabled-win32-tpm.md)<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | Desabilite o TPM.<br/> Essa operação é revertida pela operação 1.<br/> Para obter mais informações, consulte o seguinte método relacionado que não envolve a presença física: [**Desabilitar**](disable-win32-tpm.md).<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | Ative o TPM.<br/> Essa operação é invertida pela operação 4.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | Desative o TPM.<br/> Essa operação é invertida pela operação 3.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | Limpe o TPM.<br/> Essa operação não pode ser revertida.<br/> Para obter mais informações, consulte o seguinte método relacionado que não envolve a presença física: [**Limpar**](clear-win32-tpm.md).<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | Habilita e ativa o TPM.<br/> Essa operação é invertida pela operação 7.<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | Desative e desabilite o TPM.<br/> Essa operação é invertida pela operação 6.<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | Permitir a instalação de um proprietário do TPM.<br/> Essa operação é invertida pela operação 9.<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | Impedir a instalação de um proprietário do TPM.<br/> Essa operação é invertida pela operação 8. <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | Habilitar, ativar e permitir a instalação de um proprietário do TPM.<br/> Essa operação é revertida pela operação 11.<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | Desative, desabilite e impeça a instalação de um proprietário do TPM.<br/> Essa operação é revertida pela operação 10.<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | Presença física adiadaunownedFieldUpgrade<br/> A configuração de presença física foi atualizada.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Não há suporte para esse valor.<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | Limpe, habilita e ative o TPM.<br/> Essa operação não pode ser revertida.<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ False<br/> Define o provisionamento que você deve estar fisicamente presente para definir o TPM.<br/> Essa operação é invertida pela operação 16.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Não há suporte para esse valor.<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ True<br/> Define o provisionamento que você não precisa estar fisicamente presente para definir o TPM.<br/> Essa operação é revertida pela operação 15.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Não há suporte para esse valor.<br/> |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ False<br/> Define o provisionamento que você deve estar fisicamente presente para limpar o TPM.<br/> Essa operação é invertida pela operação 18.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Não há suporte para esse valor.<br/>           |
| <dl> <dt>18</dt> </dl>                                                       | SetNoPPIClear \_ True<br/> Define o provisionamento que você não precisa estar fisicamente presente para limpar o TPM.<br/> Essa operação é invertida pela operação 17.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Não há suporte para esse valor.<br/>   |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ False<br/> Define o provisionamento que você deve estar fisicamente presente para manter o TPM.<br/> Essa operação é invertida pela operação 20.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Não há suporte para esse valor.<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ True<br/> Define o provisionamento que você não precisa estar fisicamente presente para manter o TPM.<br/> Essa operação é invertida pela operação 19.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Não há suporte para esse valor.<br/>   |
| <dl> <dt>21</dt> </dl>                                                       | Habilitar + Ativar + Limpar<br/> Habilitar, ativar e limpar o TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Não há suporte para esse valor.<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | Habilitar + Ativar + Limpar + Habilitar + Ativar<br/> Habilita, ativa e limpa o TPM e, em seguida, habilita e reativa o TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Não há suporte para esse valor.<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Todos os erros do TPM, bem como erros específicos dos Serviços Base do TPM, podem ser retornados.



| Valor/código de retorno                                                                                                                                                                       | Descrição                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | O método foi bem-sucedido.<br/> Use o [**método GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) para determinar a próxima etapa necessária.<br/>                                                  |
| <dl> <dt>**TPM \_ E \_ PPI \_ SEM SUPORTE \_ 2150171395**</dt> <dt>(0x80290303)</dt> </dl> | O computador não dá suporte a operações de presença física do TPM usando esse método.<br/> Consulte o fabricante do computador para obter mais informações. O BIOS do computador pode ter suporte alternativo para configurar o TPM.<br/> |
| <dl> <dt>**TPM \_ E \_ PPI \_ ACPI \_ FAILURE 2150171392**</dt> <dt>(0x80290300)</dt> </dl>  | Ocorreu uma falha de hardware.<br/> Consulte o fabricante do computador para obter mais informações.<br/>                                                                                                                                  |



 

## <a name="remarks"></a>Comentários

As operações de presença física do TPM não exigem autorização de proprietário do TPM. No entanto, eles exigem etapas adicionais para ajudar a proteger contra alterações não autorizadas no TPM.

Computadores que suportam operações de presença física do TPM tentarão detectar o usuário fisicamente presente antes de executar a operação. Embora os computadores possam ser diferentes em como essa detecção é executada, a ideia é fazer com que um usuário ou administrador fisicamente presente autorize a operação.

Por exemplo, o computador pode exigir que o usuário reinicie o computador. Depois que o computador for reiniciado, o computador poderá exibir uma caixa de diálogo de confirmação do BIOS que permite que o usuário confirme a operação usando o teclado.

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

[**Habilitar**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Desabilitar**](disable-win32-tpm.md)
</dt> <dt>

[**Limpar**](clear-win32-tpm.md)
</dt> </dl>

 

 
