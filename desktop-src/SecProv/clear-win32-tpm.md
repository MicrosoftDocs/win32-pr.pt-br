---
description: Redefine o TPM para seu estado de fábrica-padrão.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Método Clear da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c9c3185fceb315cf9c36caa7de1e450820ad25ce1b31fefc8135c4d57fd76597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892643"
---
# <a name="clear-method-of-the-win32_tpm-class"></a>Método Clear da classe do \_ TPM do Win32

O método **Clear** da classe [**do \_ TPM do Win32**](win32-tpm.md) redefine o TPM para seu estado de fábrica padrão. Um proprietário do TPM pode usar esse método para cancelar a propriedade do TPM e invalidar materiais criptográficos criados pelo proprietário anterior. Esse método suspende o BitLocker se a chamada puder fazer com que a recuperação do BitLocker seja necessária. O BitLocker será retomado automaticamente depois que o TPM tiver sido provisionado.

> [!Caution]  
> Ao limpar o TPM, você perderá todas as chaves do TPM criadas e usadas pelos aplicativos. Se essas chaves foram usadas para criptografar dados, verifique se você tem outra maneira de acessar os dados antes de limpar o TPM.

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OwnerAuth* \[ em, opcional\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que identifica o proprietário do TPM. Essa cadeia de caracteres deve ser uma cadeia de caracteres codificada em base64 que contenha exatamente 20 bytes de dados binários. Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma frase secreta nesse formato esperado. O parâmetro *OwnerAuth* será lido no registro se nenhum for fornecido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

A tabela a seguir lista alguns dos códigos de retorno comuns.



| Código/valor de retorno                                                                                                                                                                         | Descrição                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | O método foi bem-sucedido.<br/>                                                                                                                                                |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>              | O valor de autorização do proprietário fornecido não pode executar a solicitação.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ defender \_ bloqueio \_ em execução**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | O TPM está se defendendo contra ataques de dicionário e está em um período de tempo limite. Para obter mais informações, consulte o método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/> |



 

## <a name="remarks"></a>Comentários

A execução desse método pode ajudar a preparar um computador equipado com TPM para reciclagem.

Para limpar o TPM, mas não tiver mais a autorização de proprietário do TPM, você precisa de acesso físico ao computador. O método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) inclui funcionalidade para ajudar a limpar o TPM sem autorização de proprietário do TPM.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                      |
| Namespace<br/>                | \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
