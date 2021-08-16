---
description: CAPICOM não habilita a verificação de revogação de certificado por padrão.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Verificando o status de revogação de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf1ce98e392da94fd800316fe63c5b79c8572a319c6db4246e7907eb80966d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769528"
---
# <a name="checking-certificate-revocation-status"></a>Verificando o status de revogação de certificado

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, [consulte Alternativas ao uso de CAPICOM.](alternatives-to-using-capicom.md)\]

CAPICOM não habilita a verificação de revogação de certificado por padrão. No entanto, a verificação de revogação de certificado pode ser habilitada programaticamente para um certificado específico por meio da propriedade **IsValid.CheckFlag** de um objeto Certificate. Depois que o valor apropriado de **CheckFlag** tiver sido definido, acessar a propriedade **IsValid.Result** do objeto de certificado ou criar o caminho de verificação do certificado usando o método Build de um objeto Chain força a verificação de revogação.

No exemplo a seguir, o certificado foi instautado como um certificado CAPICOM válido.


```VB
Dim cert As Certificate
Dim LocalStore As New Store

' Open the My store.
LocalStore.Open LocalStore.Open CAPICOM_CURRENT_USER_STORE, _
    CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_WRITE

' Get the first certificate in the My store.
set cert = LocalStore.Certificates.Item(1)

cert.IsValid.CheckFlag = CAPICOM_CHECK_TRUSTED_ROOT Or _ 
   CAPICOM_CHECK_TIME_VALIDITY Or _ 
   CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
   CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
If cert.IsValid.Result Then
'CERTIFICATE IS VALID!
Else
Dim chain As New Chain
     chain.Build (cert)
     If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
     End If
     If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
'THE REVOCATION STATUS COULD NOT BE DETERMINED
     End If
End If

```



O anterior se aplica a um certificado individual, independentemente de como ele foi obtido. A execução da verificação de revogação nos certificados em um objeto [**SignedData**](signeddata.md) não é diferente porque o método [**Verify**](signeddata-verify.md) do objeto **SignedData** não pode ser usado para essa finalidade, pois a habilitação de CAPICOM VERIFY SIGNATURE AND CERTIFICATE não causa a verificação \_ de \_ \_ \_ CRL.

Em vez disso, **o CheckFlag** deve ser definido para o certificado de cada signante. Considere o exemplo a seguir em que sData foi instautado como um objeto CAPICOM [**SignedData**](signeddata.md) válido.


```VB
Dim cert As Certificate
Dim chain As New Chain

' sData is an existing SignedData object.

For I = 1 To sData.Certificates.Count
   set cert = sData.Certificates(I) 
   cert.IsValid.CheckFlag = _ 
       CAPICOM_CHECK_TRUSTED_ROOT Or _ 
       CAPICOM_CHECK_TIME_VALIDITY Or _ 
       CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
       CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
   If cert.IsValid.Result Then
      'THE CERTIFICATE IS VALID!
   Else
      chain.Build cert
      If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
         'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
      End If
      If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
         'THE REVOCATION STATUS COULD NOT BE DETERMINED
      End If
   End If
Next I
```



O exemplo adicional é o loop sobre todos os certificados no [**objeto SignedData.**](signeddata.md)

 

 



