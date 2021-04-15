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
ms.openlocfilehash: 55a0f8c5fc0a8573192f25e3901b63f24e05f7c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753717"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Método SetPhysicalPresenceRequest da classe Win32 \_ TPM

O método **SetPhysicalPresenceRequest** da classe [**\_ TPM do Win32**](win32-tpm.md) solicita uma operação do TPM que requer presença física. Depois de usar esse método para enviar uma solicitação, aplique a próxima etapa indicada no método [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) . Por fim, use o método [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) para verificar se a operação foi executada com êxito. Esse método suspende o BitLocker se a chamada puder fazer com que a recuperação do BitLocker seja necessária. O BitLocker será retomado automaticamente depois que o TPM tiver sido provisionado.

Essas etapas são necessárias porque as operações de presença física podem ser executadas somente depois que o computador detectar o usuário fisicamente presente.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Solicitação* \[ do no\]
</dt> <dd>

Tipo: **UInt32**

Um valor inteiro que especifica a operação de TPM solicitada que requer a presença física.



| Valor                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | Nenhuma solicitação.<br/> Use esse valor para limpar uma solicitação pendente.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | Habilite o TPM.<br/> Esta operação é revertida pela operação 2.<br/> Para obter mais informações, consulte os seguintes métodos relacionados que não envolvem a presença física: [**habilitar**](enable-win32-tpm.md) e [**IsEnabled**](isenabled-win32-tpm.md).<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | Desabilite o TPM.<br/> Esta operação é revertida pela operação 1.<br/> Para obter mais informações, consulte o seguinte método relacionado que não envolve a presença física: [**desabilitar**](disable-win32-tpm.md).<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | Ative o TPM.<br/> Esta operação é revertida pela operação 4.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | Desativar o TPM.<br/> Esta operação é revertida pela operação 3.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | Limpe o TPM.<br/> Esta operação não pode ser revertida.<br/> Para obter mais informações, consulte o seguinte método relacionado que não envolve a presença física: [**Clear**](clear-win32-tpm.md).<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | Habilitar e ativar o TPM.<br/> Esta operação é revertida pela operação 7.<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | Desativar e desabilitar o TPM.<br/> Esta operação é revertida pela operação 6.<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | Permitir a instalação de um proprietário do TPM.<br/> Esta operação é revertida pela operação 9.<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | Impedir a instalação de um proprietário do TPM.<br/> Esta operação é revertida pela operação 8. <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | Habilite, ative e permita a instalação de um proprietário do TPM.<br/> Esta operação é revertida pela operação 11.<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | Desativar, desabilitar e impedir a instalação de um proprietário do TPM.<br/> Esta operação é revertida pela operação 10.<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | PresenceunownedFieldUpgrade físico adiado<br/> A configuração de presença física foi atualizada.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Não há suporte para esse valor.<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | Limpar, habilitar e ativar o TPM.<br/> Esta operação não pode ser revertida.<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ false<br/> Define o provisionamento que você deve estar fisicamente presente para definir o TPM.<br/> Esta operação é revertida pela operação 16.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Não há suporte para esse valor.<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ true<br/> Define o provisionamento de que você não precisa estar fisicamente presente para definir o TPM.<br/> Esta operação é revertida pela operação 15.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Não há suporte para esse valor.<br/> |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ false<br/> Define o provisionamento que você deve estar fisicamente presente para limpar o TPM.<br/> Esta operação é revertida pela operação 18.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Não há suporte para esse valor.<br/>           |
| <dl> <dt>anos</dt> </dl>                                                       | SetNoPPIClear \_ true<br/> Define o provisionamento que você não precisa estar fisicamente presente para limpar o TPM.<br/> Esta operação é revertida pela operação 17.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Não há suporte para esse valor.<br/>   |
| <dl> <dt>aprimora</dt> </dl>                                                       | SetNoPPIMaintenance \_ false<br/> Define o provisionamento que você deve estar fisicamente presente para manter o TPM.<br/> Esta operação é revertida pela operação 20.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Não há suporte para esse valor.<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ true<br/> Define o provisionamento de que você não precisa estar fisicamente presente para manter o TPM.<br/> Esta operação é revertida pela operação 19.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Não há suporte para esse valor.<br/>   |
| <dl> <dt>Abril</dt> </dl>                                                       | Habilitar + ativar + limpar<br/> Habilitar, ativar e limpar o TPM.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Não há suporte para esse valor.<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | Habilitar + ativar + limpar + habilitar + ativar<br/> Habilite, ative e limpe o TPM e, em seguida, habilite e reative o TPM.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Não há suporte para esse valor.<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.



| Código/valor de retorno                                                                                                                                                                       | Descrição                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | O método foi bem-sucedido.<br/> Use o método [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) para determinar a próxima etapa necessária.<br/>                                                  |
| <dl> <dt>**TPM \_ \_ \_ Não \_ há suporte para E PPI**</dt> <dt>2150171395 (0x80290303)</dt> </dl> | O computador não oferece suporte a operações de presença física de TPM usando esse método.<br/> Consulte o fabricante do seu computador para obter mais informações. O BIOS do computador pode ter suporte alternativo para configurar o TPM.<br/> |
| <dl> <dt>**TPM \_ \_Falha de \_ ACPI \_ PPI**</dt> <dt>2150171392 (0x80290300)</dt> </dl>  | Ocorreu uma falha de hardware.<br/> Consulte o fabricante do seu computador para obter mais informações.<br/>                                                                                                                                  |



 

## <a name="remarks"></a>Comentários

As operações de presença física do TPM não exigem autorização de proprietário do TPM. No entanto, eles exigem etapas adicionais para ajudar a proteger contra alterações não autorizadas no TPM.

Os computadores que dão suporte a operações de presença física do TPM tentarão detectar o usuário fisicamente presente antes de executar a operação. Embora os computadores possam diferir em como essa detecção é executada, a ideia é ter um usuário ou administrador fisicamente presente na operação.

Por exemplo, o computador pode exigir que o usuário reinicie o computador. Depois que o computador for reiniciado, o computador poderá exibir uma caixa de diálogo de confirmação do BIOS que permite ao usuário confirmar a operação usando o teclado.

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

[**Habilitar**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Desabilitar**](disable-win32-tpm.md)
</dt> <dt>

[**Formatação**](clear-win32-tpm.md)
</dt> </dl>

 

 
