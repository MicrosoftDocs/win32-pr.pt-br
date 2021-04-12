---
description: O CAPICOM não habilita a verificação de revogação de certificado por padrão.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Verificando o status de revogação do certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada134bbca88b1a875ff27add7566116cf7334bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170779"
---
# <a name="checking-certificate-revocation-status"></a><span data-ttu-id="ece41-103">Verificando o status de revogação do certificado</span><span class="sxs-lookup"><span data-stu-id="ece41-103">Checking Certificate Revocation Status</span></span>

<span data-ttu-id="ece41-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ece41-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ece41-105">Em vez disso, use o .NET Framework para implementar recursos de segurança.</span><span class="sxs-lookup"><span data-stu-id="ece41-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="ece41-106">Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="ece41-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="ece41-107">O CAPICOM não habilita a verificação de revogação de certificado por padrão.</span><span class="sxs-lookup"><span data-stu-id="ece41-107">CAPICOM does not enable certificate revocation checking by default.</span></span> <span data-ttu-id="ece41-108">No entanto, a verificação de revogação de certificado pode ser habilitada programaticamente para um certificado específico por meio da propriedade **IsValid. CheckFlag** de um objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="ece41-108">However, certificate revocation checking can be enabled programmatically for a particular certificate through the **IsValid.CheckFlag** property of a Certificate object.</span></span> <span data-ttu-id="ece41-109">Depois que o valor apropriado de **CheckFlag** tiver sido definido, acessar a propriedade **IsValid. Result** do objeto de certificado ou criar o caminho de verificação do certificado usando um método de criação do objeto de cadeia forçará a verificação de revogação.</span><span class="sxs-lookup"><span data-stu-id="ece41-109">After the appropriate value of **CheckFlag** has been set, accessing the Certificate object's **IsValid.Result** property or building the certificate's verification path using a Chain object's Build method forces revocation checking.</span></span>

<span data-ttu-id="ece41-110">No exemplo a seguir, o certificado foi instanciado como um certificado capicor válido.</span><span class="sxs-lookup"><span data-stu-id="ece41-110">In the following example, cert has been instantiated as a valid CAPICOM certificate.</span></span>


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



<span data-ttu-id="ece41-111">O anterior se aplica a um certificado individual, independentemente de como ele foi obtido.</span><span class="sxs-lookup"><span data-stu-id="ece41-111">The preceding applies to an individual certificate, no matter how it was obtained.</span></span> <span data-ttu-id="ece41-112">Executar a verificação de revogação nos certificados em um objeto [**SignedData**](signeddata.md) não é diferente porque o método [**Verify**](signeddata-verify.md) do objeto **SignedData** não pode ser usado para essa finalidade porque a habilitação de CAPICOM a \_ \_ assinatura e o \_ \_ certificado não causam a verificação da CRL.</span><span class="sxs-lookup"><span data-stu-id="ece41-112">Performing revocation checking on the certificates in a [**SignedData**](signeddata.md) object is no different because the **SignedData** object's [**Verify**](signeddata-verify.md) method cannot be used for this purpose because enabling CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE does not cause CRL checking.</span></span>

<span data-ttu-id="ece41-113">Em vez disso, o **CheckFlag** deve ser definido para o certificado de cada signatário.</span><span class="sxs-lookup"><span data-stu-id="ece41-113">Instead, the **CheckFlag** must be set for each signer's certificate.</span></span> <span data-ttu-id="ece41-114">Considere o exemplo a seguir, em que sData foi instanciado como um objeto [**SignedData**](signeddata.md) de CAPICOM válido.</span><span class="sxs-lookup"><span data-stu-id="ece41-114">Consider the following example where sData has been instantiated as a valid CAPICOM [**SignedData**](signeddata.md) object.</span></span>


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



<span data-ttu-id="ece41-115">O exemplo adicional é o loop sobre todos os certificados no objeto [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="ece41-115">The additional example is the loop over all the certificates in the [**SignedData**](signeddata.md) object.</span></span>

 

 



