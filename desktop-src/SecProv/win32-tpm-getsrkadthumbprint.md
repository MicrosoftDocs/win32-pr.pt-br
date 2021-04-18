---
description: Obtém a impressão digital da chave raiz de armazenamento para um determinado módulo da parte pública da chave raiz de armazenamento do TPM.
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
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762902"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a>\_Método TPM:: GetSrkADThumbprint do Win32

Obtém a impressão digital da chave raiz de armazenamento para um determinado módulo da parte pública da chave raiz de armazenamento do TPM. A impressão digital é usada para indexar as chaves raiz de armazenamento no servidor de Active Directory se o Active Directory backup das informações de autorização do proprietário do TPM for habilitado por meio da configuração Política de Grupo.

> [!Note]  
> A partir do Windows 10, versão 1607, a autorização do proprietário do TPM nunca é submetida a backup em Active Directory.

 

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

O módulo da parte pública da chave raiz de armazenamento do TPM. Ele também pode ser obtido usando o método [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) da classe [Win32 \_ TPM](win32-tpm.md) .

</dd> <dt>

*SrkADThumbprint* \[ fora\]
</dt> <dd>

Retorna uma matriz de 20 bytes que contém a impressão digital da chave raiz de armazenamento para o módulo fornecido.

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

 

 
