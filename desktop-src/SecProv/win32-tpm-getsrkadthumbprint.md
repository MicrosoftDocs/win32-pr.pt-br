---
description: obtém a impressão digital de Armazenamento chave raiz para um determinado módulo da parte pública do TPM Armazenamento chave raiz.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Método Win32_Tpm:: GetSrkADThumbprint'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9be4b7f02a9b645c29b431a9d974f5871ad5a95fc001e43df17bfe459483974e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004104"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>\_Método TPM:: GetSrkADThumbprint do Win32

obtém a impressão digital de Armazenamento chave raiz para um determinado módulo da parte pública do TPM Armazenamento chave raiz. a impressão digital é usada para indexar as chaves raiz Armazenamento no servidor Active Directory se o backup Active Directory de informações de autorização de proprietário do TPM estiver habilitado por meio da configuração Política de Grupo.

> [!Note]  
> a partir do Windows 10, versão 1607, a autorização do proprietário do TPM nunca é submetida a backup em Active Directory.

 

Esse método só pode ser acessado por administradores locais.

## <a name="syntax"></a>Sintaxe


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SrkPublicKeyModulus* \[ no\]
</dt> <dd>

o módulo da parte pública do TPM Armazenamento chave raiz. Ele também pode ser obtido usando o método [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) da classe [Win32 \_ TPM](win32-tpm.md) .

</dd> <dt>

*SrkADThumbprint* \[ fora\]
</dt> <dd>

Retorna uma matriz de 20 bytes que contém a impressão digital da chave raiz de armazenamento para o módulo fornecido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
