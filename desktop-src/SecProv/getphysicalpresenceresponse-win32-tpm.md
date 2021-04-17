---
description: Retorna os resultados de uma operação de presença física de TPM que foi executada.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Método GetPhysicalPresenceResponse da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 47dfad1491b398b035e40867d10d2d3e46327dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780153"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a>Método GetPhysicalPresenceResponse da classe Win32 \_ TPM

O método **GetPhysicalPresenceResponse** da classe [**Win32 \_ TPM**](win32-tpm.md) retorna os resultados de uma operação de presença física de TPM que foi executada. Use o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Solicitação* \[ do fora\]
</dt> <dd>

Tipo: **UInt32**

Um valor inteiro que especifica a operação de presença física do TPM que foi executada.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>0</dt> </dl></td>
<td>Nenhuma solicitação.<br/> Nenhuma operação de presença física foi executada.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1</dt> </dl></td>
<td>Habilite o TPM.<br/> Esta operação é revertida pela operação 2. <br/> Para obter mais informações, consulte estes métodos relacionados que não envolvem a presença física:
<ul>
<li><a href="enable-win32-tpm.md"><strong>Habilitar</strong></a></li>
<li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>2</dt> </dl></td>
<td>Desabilite o TPM.<br/> Esta operação é revertida pela operação 1. <br/> Para obter mais informações, consulte este método relacionado que não envolve a presença física: <a href="disable-win32-tpm.md"><strong>desabilitar</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>Beta</dt> </dl></td>
<td>Ative o TPM.<br/> Esta operação é revertida pela operação 4.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>quatro</dt> </dl></td>
<td>Desativar o TPM.<br/> Esta operação é revertida pela operação 3.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>05</dt> </dl></td>
<td>Limpe o TPM.<br/> Esta operação não pode ser revertida. <br/> Para obter mais informações, consulte este método relacionado que não envolve a presença física: <a href="clear-win32-tpm.md"><strong>claro</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>152</dt> </dl></td>
<td>Habilitar e ativar o TPM.<br/> Esta operação é revertida pela operação 7.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>7</dt> </dl></td>
<td>Desativar e desabilitar o TPM.<br/> Esta operação é revertida pela operação 6. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>8</dt> </dl></td>
<td>Permitir a instalação de um proprietário do TPM.<br/> Esta operação é revertida pela operação 9.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>99</dt> </dl></td>
<td>Impedir a instalação de um proprietário do TPM.<br/> Esta operação é revertida pela operação 8. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>254</dt> </dl></td>
<td>Habilite, ative e permita a instalação de um proprietário do TPM.<br/> Esta operação é revertida pela operação 11.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>11</dt> </dl></td>
<td>Desativar, desabilitar e impedir a instalação de um proprietário do TPM.<br/> Esta operação é revertida pela operação 10.<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>PresenceunownedFieldUpgrade físico adiado<br/> A configuração de presença física foi atualizada.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>140</dt> </dl></td>
<td>Limpar, habilitar e ativar o TPM.<br/> Esta operação não pode ser revertida.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>15</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> Define o provisionamento que você deve estar fisicamente presente para definir o TPM.<br/> Esta operação é revertida pela operação 16.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>16</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> Define o provisionamento de que você não precisa estar fisicamente presente para definir o TPM.<br/> Esta operação é revertida pela operação 15.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>16</dt> </dl></td>
<td>SetNoPPIClear_False<br/> Define o provisionamento que você deve estar fisicamente presente para limpar o TPM.<br/> Esta operação é revertida pela operação 18.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>anos</dt> </dl></td>
<td>SetNoPPIClear_True<br/> Define o provisionamento que você não precisa estar fisicamente presente para limpar o TPM.<br/> Esta operação é revertida pela operação 17.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>aprimora</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> Define o provisionamento que você deve estar fisicamente presente para manter o TPM.<br/> Esta operação é revertida pela operação 20.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>20,00</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> Define o provisionamento que você deve estar fisicamente presente para manter o TPM.<br/> Esta operação é revertida pela operação 19.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>Abril</dt> </dl></td>
<td>Habilitar + ativar + limpar<br/> Habilitar, ativar e limpar o TPM.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>22</dt> </dl></td>
<td>Habilitar + ativar + limpar + habilitar + ativar<br/> Habilite, ative e limpe o TPM e, em seguida, habilite e reative o TPM.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*Resposta* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Um valor inteiro que especifica os resultados da execução da operação de presença física do TPM.

Uma operação de presença física será bem-sucedida se um usuário presente fisicamente confirmar a operação e se a operação for executada sem erros.

Esse valor pode conter qualquer erro de TPM. A tabela a seguir lista algumas das respostas de erro comuns.



| Valor                                                                                                                                                                                                                                                                    | Significado                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                                                                                                                                                             | A operação do TPM solicitada foi bem-sucedida.<br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <dt>**TPM \_ E/ \_ PPI \_ usuário \_ anular**</dt> <dt>2150171393 (0x80290301)</dt> </dl>       | O usuário rejeitou a operação de TPM solicitada.<br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <dt>**TPM \_ \_Falha de \_ BIOS \_ E PPI**</dt> <dt>2150171394 (0x80290302)</dt> </dl> | Ocorreu uma falha do BIOS ao executar a operação do TPM.<br/> |



 

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

[**Formatação**](clear-win32-tpm.md)
</dt> <dt>

[**Desabilitar**](disable-win32-tpm.md)
</dt> <dt>

[**Habilitar**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> </dl>

 

 
