---
description: Redefine o período de tempo limite ou outro mecanismo que os fabricantes do TPM implementam para proteger contra ataques de dicionário em valores de autorização do TPM.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Método ResetAuthLockOut da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756556"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a>Método ResetAuthLockOut da classe Win32 \_ TPM

O método **ResetAuthLockOut** da classe [**do \_ TPM do Win32**](win32-tpm.md) redefine o período de tempo limite ou outro mecanismo que os fabricantes do TPM implementam para proteger contra ataques de dicionário em valores de autorização do TPM. Em um ataque de dicionário, um invasor tenta adivinhar um valor de autorização do TPM correto, tentando exaustivamente todos os valores possíveis.

Use esse método se o TPM estiver bloqueado devido a muitas tentativas incorretas na inserção da autorização do proprietário ou de outros valores de autorização. Quando o TPM estiver bloqueado, alguns ou todos os comandos emitidos para o TPM retornarão um erro, o TPM \_ E \_ defenderão o \_ bloqueio \_ em execução (0x80280803).

> [!Note]  
> Esse método só pode ser usado exatamente uma vez quando o TPM é bloqueado. Se a autorização de proprietário fornecida para esse método estiver incorreta, o TPM será bloqueado durante todo o período de tempo limite e as tentativas adicionais na redefinição do bloqueio falharão.

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OwnerAuth* \[ em, opcional\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que identifica o proprietário do TPM.

Essa cadeia de caracteres deve ser uma cadeia de caracteres terminada em NULL codificada em base64 que contenha exatamente 20 bytes de dados binários. Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma frase secreta nesse formato esperado. O parâmetro *OwnerAuth* será lido no registro se nenhum for fornecido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados. A tabela a seguir lista alguns dos valores de retorno comuns.



| Código/valor de retorno                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                            | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl> | O valor de autorização do proprietário fornecido está incorreto. Tentativas adicionais na redefinição do bloqueio falharão com esse mesmo erro. Aguarde até que o período de tempo limite ou outro mecanismo específico do fabricante tenha expirado antes de tentar novamente os comandos bloqueados do TPM.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o \_ comando ResetLockValue do TPM no TPM. O comportamento exato desse método varia entre os fabricantes do TPM. A documentação do fabricante do computador ou TPM pode fornecer informações adicionais sobre a implementação do mecanismo de ataque do anti-dicionário.

Em geral, os fabricantes podem detectar ataques de dicionário mantendo o controle das autenticações com falha. Se o número ou a frequência de falhas se tornarem alta o suficiente, o TPM bloqueará outros comandos por um determinado tempo. Em geral, o período de tempo limite inicial será curto, para permitir que um usuário legítimo a oportunidade de corrigir a situação. Se as falhas continuarem, a duração de cada período de tempo limite subsequente pode aumentar rapidamente.

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
</dt> </dl>

 

 
