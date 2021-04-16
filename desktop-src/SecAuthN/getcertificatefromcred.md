---
description: Obtém o certificado da credencial do usuário.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Função GetCertificateFromCred (Lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747243"
---
# <a name="getcertificatefromcred-function"></a>Função GetCertificateFromCred

Obtém o certificado da credencial do usuário.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProviderHandle* \[ no\]
</dt> <dd>

Identificador do provedor de identidade.

</dd> <dt>

*ClientToken* \[ no\]
</dt> <dd>

Token do chamador que está recuperando o certificado.

</dd> <dt>

*SuppliedCred* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ credencial fornecida pelo SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) que contém a credencial de uma ID online cujo certificado é solicitado. O provedor de identidade deve validar os dados de entrada como se eles esvenham de uma fonte não confiável.

</dd> <dt>

*SuppliedCredSize* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *SuppliedCred* .

</dd> <dt>

*CertContext* \[ fora\]
</dt> <dd>

Se a função for realizada com sucesso, esse parâmetro será um ponteiro para o \_ ponteiro de contexto CCERT retornado. Quando você terminar de usar o contexto do certificado, libere-o chamando a função [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, a função retornará o STATUS \_ êxito.

Se a função falhar, a função poderá retornar um dos seguintes códigos de erro de NTSTATUS.



| Valor retornado                                                                                            | Descrição                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>STATUS \_ sem \_ suporte</dt> </dl>       | O provedor de identidade não reconhece o tipo de credencial da credencial fornecida. O LSA tentará o próximo provedor de identidade.<br/>                                           |
| <dl> <dt>\_falha de logon de status \_</dt> </dl>       | A credencial está incorreta.<br/>                                                                                                                                                |
| <dl> <dt>parâmetro de STATUS \_ inválido \_</dt> </dl>   | Um parâmetro não é válido. A credencial pode estar em um formato incorreto e não na estrutura de [**\_ \_ credenciais fornecida pelo SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) definido.<br/> |
| <dl> <dt>rede de STATUS \_ \_ inacessível</dt> </dl> | O provedor de identidade não pode entrar em contato com a nuvem para obter o certificado.<br/>                                                                                                   |
| <dl> <dt>senha de STATUS \_ \_ expirada</dt> </dl>    | A senha da conta expirou.<br/>                                                                                                                                           |
| <dl> <dt>conta de STATUS \_ \_ bloqueada \_</dt> </dl> | A conta foi bloqueada. <br/>                                                                                                                                           |
| <dl> <dt>Others</dt> </dl>                       | Outros códigos de erro específicos do provedor. <br/>                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

Antes de buscar o certificado da nuvem, o provedor de identidade deve verificar se há um certificado válido para esse usuário no repositório de certificados "MY" do usuário. Se houver um certificado válido, o provedor deverá retornar esse certificado para evitar o tráfego de rede desnecessário.

O provedor de identidade também pode armazenar o certificado em cache localmente, desde que ele seja protegido do usuário atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 

