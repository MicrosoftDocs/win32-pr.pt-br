---
description: Retorna a operação de presença física de TPM pendente. Use o método SetPhysicalPresenceRequest para solicitar uma operação.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Método GetPhysicalPresenceRequest da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d88ec523e983e60cacab57b41307381b05e8de6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481862"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Método GetPhysicalPresenceRequest da classe Win32 \_ TPM

O método **GetPhysicalPresenceRequest** da classe [**Win32 \_ TPM**](win32-tpm.md) retorna a operação de presença física de TPM pendente. Use o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar uma operação.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Solicitação* \[ do fora\]
</dt> <dd>

Tipo: **UInt32**

Um valor que especifica a operação de presença física de TPM pendente.




| Valor | Significado | 
|-------|---------|
| <dl><dt>0</dt></dl> | Nenhuma solicitação.<br /> | 
| <dl><dt>1</dt></dl> | Habilite o TPM.<br /> Esta operação é revertida pela operação 2. <br /> Para obter mais informações, consulte estes métodos relacionados que não envolvem a presença física:<ul><li><a href="enable-win32-tpm.md"><strong>Habilitar</strong></a></li><li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li></ul><br /> | 
| <dl><dt>2</dt></dl> | Desabilite o TPM.<br /> Esta operação é revertida pela operação 1. <br /> Para obter mais informações, consulte este método relacionado que não envolve a presença física: <a href="disable-win32-tpm.md"><strong>desabilitar</strong></a>.<br /> | 
| <dl><dt>3</dt></dl> | Ative o TPM.<br /> Esta operação é revertida pela operação 4.<br /> | 
| <dl><dt>4</dt></dl> | Desativar o TPM.<br /> Esta operação é revertida pela operação 3.<br /> | 
| <dl><dt>5</dt></dl> | Limpe o TPM.<br /> Esta operação não pode ser revertida.<br /> Para obter mais informações, consulte este método relacionado que não envolve a presença física: <a href="clear-win32-tpm.md"><strong>claro</strong></a>.<br /> | 
| <dl><dt>6</dt></dl> | Habilitar e ativar o TPM. <br /> Esta operação é revertida pela operação 7.<br /> | 
| <dl><dt>7</dt></dl> | Desativar e desabilitar o TPM.<br /> Esta operação é revertida pela operação 6. <br /> | 
| <dl><dt>8</dt></dl> | Permitir a instalação de um proprietário do TPM. <br /> Esta operação é revertida pela operação 9.<br /> | 
| <dl><dt>9</dt></dl> | Impedir a instalação de um proprietário do TPM.<br /> Esta operação é revertida pela operação 8. <br /> | 
| <dl><dt>10</dt></dl> | Habilite, ative e permita a instalação de um proprietário do TPM.<br /> Esta operação é revertida pela operação 11.<br /> | 
| <dl><dt>11</dt></dl> | Desativar, desabilitar e impedir a instalação de um proprietário do TPM.<br /> Esta operação é revertida pela operação 10.<br /> | 
| <span></span><dl><dt><strong></strong></dt><dt>12</dt></dl> | PresenceunownedFieldUpgrade físico adiado<br /> A configuração de presença física foi atualizada.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br /> | 
| <dl><dt>14</dt></dl> | Limpar, habilitar e ativar o TPM.<br /> Esta operação não pode ser revertida.<br /> | 
| <dl><dt>15</dt></dl> | SetNoPPIProvision_False<br /> Define o provisionamento que você deve estar fisicamente presente para definir o TPM.<br /> Esta operação é revertida pela operação 16.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br /> | 
| <dl><dt>16</dt></dl> | SetNoPPIProvision_True<br /> Define o provisionamento de que você não precisa estar fisicamente presente para definir o TPM.<br /> Esta operação é revertida pela operação 15.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br /> | 
| <dl><dt>17</dt></dl> | SetNoPPIClear_False<br /> Define o provisionamento que você deve estar fisicamente presente para limpar o TPM.<br /> Esta operação é revertida pela operação 18.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br /> | 
| <dl><dt>anos</dt></dl> | SetNoPPIClear_True<br /> Define o provisionamento que você não precisa estar fisicamente presente para limpar o TPM.<br /> Esta operação é revertida pela operação 17.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br /> | 
| <dl><dt>19</dt></dl> | SetNoPPIMaintenance_False<br /> Define o provisionamento que você deve estar fisicamente presente para manter o TPM.<br /> Esta operação é revertida pela operação 20.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br /> | 
| <dl><dt>20</dt></dl> | SetNoPPIMaintenance_True<br /> Define o provisionamento que você deve estar fisicamente presente para manter o TPM.<br /> Esta operação é revertida pela operação 19.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br /> | 
| <dl><dt>Abril</dt></dl> | Habilitar + ativar + limpar<br /> Habilitar, ativar e limpar o TPM.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br /> | 
| <dl><dt>22</dt></dl> | Habilitar + ativar + limpar + habilitar + ativar<br /> Habilite, ative e limpe o TPM e, em seguida, habilite e reative o TPM.<br /><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Não há suporte para esse valor.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos dos Serviços Base do TPM, podem ser retornados.

A tabela a seguir lista os códigos de retorno comuns.



| Valor/código de retorno                                                                                                                                                                      | Descrição                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | O método foi bem-sucedido.<br/>                                                            |
| <dl> <dt>**TPM \_ E \_ PPI \_ ACPI \_ FAILURE**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Ocorreu uma falha de hardware. Consulte o fabricante do computador para obter mais informações.<br/> |



 

## <a name="remarks"></a>Comentários

Managed Object Format arquivos (MOF) contêm as definições para classes Windows WMI (Instrumentação de Gerenciamento). Os arquivos MOF não são instalados como parte do Windows SDK. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

[**Limpar**](clear-win32-tpm.md)
</dt> <dt>

[**Desabilitar**](disable-win32-tpm.md)
</dt> <dt>

[**Habilitar**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
