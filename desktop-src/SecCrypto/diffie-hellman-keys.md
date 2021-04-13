---
description: Explica como gerar, trocar, importar e exportar chaves de Diffie-Hellman.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Chaves de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297678"
---
# <a name="diffie-hellman-keys"></a><span data-ttu-id="1d59a-103">Chaves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="1d59a-103">Diffie-Hellman Keys</span></span>

-   [<span data-ttu-id="1d59a-104">Gerando chaves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="1d59a-104">Generating Diffie-Hellman Keys</span></span>](#generating-diffie-hellman-keys)
-   [<span data-ttu-id="1d59a-105">Trocando chaves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="1d59a-105">Exchanging Diffie-Hellman Keys</span></span>](#exchanging-diffie-hellman-keys)
-   [<span data-ttu-id="1d59a-106">Exportando uma chave privada de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="1d59a-106">Exporting a Diffie-Hellman Private Key</span></span>](#exporting-a-diffie-hellman-private-key)
-   [<span data-ttu-id="1d59a-107">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="1d59a-107">Example Code</span></span>](#example-code)

## <a name="generating-diffie-hellman-keys"></a><span data-ttu-id="1d59a-108">Gerando chaves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="1d59a-108">Generating Diffie-Hellman Keys</span></span>

<span data-ttu-id="1d59a-109">Para gerar uma chave de Diffie-Hellman, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="1d59a-109">To generate a Diffie-Hellman key, perform the following steps:</span></span>

1.  <span data-ttu-id="1d59a-110">Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="1d59a-110">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="1d59a-111">Gere a nova chave.</span><span class="sxs-lookup"><span data-stu-id="1d59a-111">Generate the new key.</span></span> <span data-ttu-id="1d59a-112">Há duas maneiras de fazer isso – com o CryptoAPI, gere todos os novos valores para G, P e X ou usando valores existentes para G e P e gerando um novo valor para X.</span><span class="sxs-lookup"><span data-stu-id="1d59a-112">There are two ways to accomplish this—by having CryptoAPI generate all new values for G, P, and X or by using existing values for G and P, and generating a new value for X.</span></span>

    <span data-ttu-id="1d59a-113">**Para gerar a chave gerando todos os novos valores**</span><span class="sxs-lookup"><span data-stu-id="1d59a-113">**To generate the key by generating all new values**</span></span>

    1.  <span data-ttu-id="1d59a-114">Chame a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , passando **CALG \_ DH \_ it** (Store e Forward) ou **CALG \_ DH \_ EPHEM** (efêmero) no parâmetro *algid* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-114">Call the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function, passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter.</span></span> <span data-ttu-id="1d59a-115">A chave será gerada usando valores novos e aleatórios para G e P, um valor calculado recentemente para X e seu identificador será retornado no parâmetro *phKey* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-115">The key will be generated using new, random values for G and P, a newly calculated value for X, and its handle will be returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="1d59a-116">A nova chave agora está pronta para uso.</span><span class="sxs-lookup"><span data-stu-id="1d59a-116">The new key is now ready for use.</span></span> <span data-ttu-id="1d59a-117">Os valores de G e P devem ser enviados ao destinatário junto com a chave (ou enviados por algum outro método) ao fazer uma [*troca de chaves*](../secgloss/e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1d59a-117">The values of G and P must be sent to the recipient along with the key (or sent by some other method) when doing a [*key exchange*](../secgloss/e-gly.md).</span></span>

    <span data-ttu-id="1d59a-118">**Para gerar a chave usando valores predefinidos para G e P**</span><span class="sxs-lookup"><span data-stu-id="1d59a-118">**To generate the key by using predefined values for G and P**</span></span>

    1.  <span data-ttu-id="1d59a-119">Chame [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passando **CALG \_ DH \_ it** (Store e Forward) ou **CALG \_ DH \_ EPHEM** (efêmero) no parâmetro *algid* e **criptografado \_ PREGEN** para o parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-119">Call [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter and **CRYPT\_PREGEN** for the *dwFlags* parameter.</span></span> <span data-ttu-id="1d59a-120">Um identificador de chave será gerado e retornado no parâmetro *phKey* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-120">A key handle will be generated and returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="1d59a-121">Inicialize uma estrutura de [**\_ \_ blob de dados criptografados**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) com o membro **PbData** definido como o valor P.</span><span class="sxs-lookup"><span data-stu-id="1d59a-121">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the P value.</span></span> <span data-ttu-id="1d59a-122">O [*blob*](../secgloss/b-gly.md) não contém informações de cabeçalho e o membro **pbData** está no formato [*little-endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1d59a-122">The [*BLOB*](../secgloss/b-gly.md) contains no header information and the **pbData** member is in [*little-endian*](../secgloss/l-gly.md) format.</span></span>
    3.  <span data-ttu-id="1d59a-123">O valor de P é definido chamando a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando o identificador de chave recuperado na etapa a no parâmetro *HKEY* , o sinalizador **KP \_ P** no parâmetro *dwParam* e um ponteiro para a estrutura que contém o valor de P no parâmetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-123">The value of P is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_P** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of P in the *pbData* parameter.</span></span>
    4.  <span data-ttu-id="1d59a-124">Inicialize uma estrutura de [**\_ \_ blob de dados criptografados**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) com o membro **PbData** definido como o valor G.</span><span class="sxs-lookup"><span data-stu-id="1d59a-124">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the G value.</span></span> <span data-ttu-id="1d59a-125">O BLOB não contém informações de cabeçalho e o membro **pbData** está no formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="1d59a-125">The BLOB contains no header information and the **pbData** member is in little-endian format.</span></span>
    5.  <span data-ttu-id="1d59a-126">O valor de G é definido chamando a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando o identificador de chave recuperado na etapa a no parâmetro *HKEY* , o sinalizador **KP \_ G** no parâmetro *dwParam* e um ponteiro para a estrutura que contém o valor de G no parâmetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-126">The value of G is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_G** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of G in the *pbData* parameter.</span></span>
    6.  <span data-ttu-id="1d59a-127">O valor de X é gerado chamando a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , passando o identificador de chave recuperado na etapa a no parâmetro *HKEY* , o sinalizador **KP \_ X** no parâmetro *dwParam* e **nulo** no parâmetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-127">The value of X is generated by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_X** flag in the *dwParam* parameter, and **NULL** in the *pbData* parameter.</span></span>
    7.  <span data-ttu-id="1d59a-128">Se todas as chamadas de função forem bem-sucedidas, a chave pública Diffie-Hellman estará pronta para uso.</span><span class="sxs-lookup"><span data-stu-id="1d59a-128">If all the function calls succeeded, the Diffie-Hellman public key is ready for use.</span></span>

3.  <span data-ttu-id="1d59a-129">Quando a chave não for mais necessária, destrua-a passando o identificador de chave para a função [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="1d59a-129">When the key is no longer needed, destroy it by passing the key handle to the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

<span data-ttu-id="1d59a-130">Se o **CALG \_ DH \_ it** tiver sido especificado nos procedimentos anteriores, os valores de chave serão persistidos no armazenamento com cada chamada para [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="1d59a-130">If **CALG\_DH\_SF** was specified in the previous procedures, the key values are persisted to storage with each call to [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span></span> <span data-ttu-id="1d59a-131">Os valores G e P podem então ser recuperados usando a função [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) .</span><span class="sxs-lookup"><span data-stu-id="1d59a-131">The G and P values can then be retrieved by using the [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) function.</span></span> <span data-ttu-id="1d59a-132">Alguns CSPs podem ter valores G e P embutidos em código.</span><span class="sxs-lookup"><span data-stu-id="1d59a-132">Some CSPs may have hard-coded G and P values.</span></span> <span data-ttu-id="1d59a-133">Nesse caso, um erro de **\_ FIXEDPARAMETER de nte** será retornado **se CryptSetKeyParam** for chamado com **KP \_ G** ou **KP \_ P** especificado no parâmetro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-133">In this case a **NTE\_FIXEDPARAMETER** error will be returned if **CryptSetKeyParam** is called with **KP\_G** or **KP\_P** specified in the *dwParam* parameter.</span></span> <span data-ttu-id="1d59a-134">Se **CryptDestroyKey** for chamado, o identificador para a chave será destruído, mas os valores de chave serão mantidos no CSP.</span><span class="sxs-lookup"><span data-stu-id="1d59a-134">If **CryptDestroyKey** is called, the handle to the key is destroyed, but the key values are retained in the CSP.</span></span> <span data-ttu-id="1d59a-135">No entanto, se **CALG \_ DH \_ EPHEM** tiver sido especificado, o identificador para a chave será destruído e todos os valores serão removidos do CSP.</span><span class="sxs-lookup"><span data-stu-id="1d59a-135">However, if **CALG\_DH\_EPHEM** was specified, the handle to the key is destroyed, and all values are cleared from the CSP.</span></span>

## <a name="exchanging-diffie-hellman-keys"></a><span data-ttu-id="1d59a-136">Trocando chaves de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="1d59a-136">Exchanging Diffie-Hellman Keys</span></span>

<span data-ttu-id="1d59a-137">A finalidade do algoritmo de Diffie-Hellman é possibilitar que duas ou mais partes criem e compartilhem uma chave de sessão secreta idêntica compartilhando informações em uma rede que não seja segura.</span><span class="sxs-lookup"><span data-stu-id="1d59a-137">The purpose of the Diffie-Hellman algorithm is to make it possible for two or more parties to create and share an identical, secret session key by sharing information over a network that is not secure.</span></span> <span data-ttu-id="1d59a-138">As informações que são compartilhadas pela rede estão na forma de alguns valores constantes e uma Diffie-Hellman chave pública.</span><span class="sxs-lookup"><span data-stu-id="1d59a-138">The information that gets shared over the network is in the form of a couple of constant values and a Diffie-Hellman public key.</span></span> <span data-ttu-id="1d59a-139">O processo usado por duas partes de troca de chaves é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1d59a-139">The process used by two key-exchange parties is as follows:</span></span>

-   <span data-ttu-id="1d59a-140">Ambas as partes concordam com os Diffie-Hellman parâmetros que são um número primo (P) e um número de gerador (G).</span><span class="sxs-lookup"><span data-stu-id="1d59a-140">Both parties agree to the Diffie-Hellman parameters which are a prime number (P) and a generator number (G).</span></span>
-   <span data-ttu-id="1d59a-141">A parte 1 envia sua Diffie-Hellman chave pública para a parte 2.</span><span class="sxs-lookup"><span data-stu-id="1d59a-141">Party 1 sends its Diffie-Hellman public key to party 2.</span></span>
-   <span data-ttu-id="1d59a-142">A parte 2 computa a chave de sessão secreta usando as informações contidas em sua chave privada e a chave pública de 1 parte.</span><span class="sxs-lookup"><span data-stu-id="1d59a-142">Party 2 computes the secret session key by using the information contained in its private key and party 1's public key.</span></span>
-   <span data-ttu-id="1d59a-143">A parte 2 envia sua Diffie-Hellman chave pública para a parte 1.</span><span class="sxs-lookup"><span data-stu-id="1d59a-143">Party 2 sends its Diffie-Hellman public key to party 1.</span></span>
-   <span data-ttu-id="1d59a-144">A parte 1 computa a chave de sessão secreta usando as informações contidas em sua chave privada e a chave pública de 2 partes.</span><span class="sxs-lookup"><span data-stu-id="1d59a-144">Party 1 computes the secret session key by using the information contained in its private key and party 2's public key.</span></span>
-   <span data-ttu-id="1d59a-145">Ambas as partes agora têm a mesma chave de sessão, que pode ser usada para criptografar e descriptografar dados.</span><span class="sxs-lookup"><span data-stu-id="1d59a-145">Both parties now have the same session key, which can be used for encrypting and decrypting data.</span></span> <span data-ttu-id="1d59a-146">As etapas necessárias para isso são mostradas no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="1d59a-146">The steps necessary for this are shown in the following procedure.</span></span>

<span data-ttu-id="1d59a-147">**Para preparar uma chave pública Diffie-Hellman para transmissão**</span><span class="sxs-lookup"><span data-stu-id="1d59a-147">**To prepare a Diffie-Hellman public key for transmission**</span></span>

1.  <span data-ttu-id="1d59a-148">Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="1d59a-148">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="1d59a-149">Crie uma chave de Diffie-Hellman chamando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para criar uma nova chave ou chamando a função [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar uma chave existente.</span><span class="sxs-lookup"><span data-stu-id="1d59a-149">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="1d59a-150">Obtenha o tamanho necessário para manter o BLOB de chave de Diffie-Hellman chamando o [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passando **NULL** para o parâmetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-150">Get the size needed to hold the Diffie-Hellman key BLOB by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passing **NULL** for the *pbData* parameter.</span></span> <span data-ttu-id="1d59a-151">O tamanho necessário será retornado em *pdwDataLen*.</span><span class="sxs-lookup"><span data-stu-id="1d59a-151">The required size will be returned in *pdwDataLen*.</span></span>
4.  <span data-ttu-id="1d59a-152">Aloque memória para o BLOB de chave.</span><span class="sxs-lookup"><span data-stu-id="1d59a-152">Allocate memory for the key BLOB.</span></span>
5.  <span data-ttu-id="1d59a-153">Crie um [*blob de chave pública*](../secgloss/p-gly.md) Diffie-Hellman chamando a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , passando **PublicKeyBlob** no parâmetro *dwBlobType* e o identificador para a chave Diffie-Hellman no parâmetro *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-153">Create a Diffie-Hellman [*public key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PUBLICKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span> <span data-ttu-id="1d59a-154">Essa chamada de função causa o cálculo do valor da chave pública, (G ^ X) mod P.</span><span class="sxs-lookup"><span data-stu-id="1d59a-154">This function call causes the calculation of the public key value, (G^X) mod P.</span></span>
6.  <span data-ttu-id="1d59a-155">Se todas as chamadas de função anteriores forem bem-sucedidas, o Diffie-Hellman BLOB de chave pública agora estará pronto para ser codificado e transmitido.</span><span class="sxs-lookup"><span data-stu-id="1d59a-155">If all the preceding function calls were successful, the Diffie-Hellman public key BLOB is now ready to be encoded and transmitted.</span></span>

<span data-ttu-id="1d59a-156">**Para importar uma chave pública Diffie-Hellman e calcular a chave de sessão secreta**</span><span class="sxs-lookup"><span data-stu-id="1d59a-156">**To import a Diffie-Hellman public key and calculate the secret session key**</span></span>

1.  <span data-ttu-id="1d59a-157">Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="1d59a-157">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="1d59a-158">Crie uma chave de Diffie-Hellman chamando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para criar uma nova chave ou chamando a função [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar uma chave existente.</span><span class="sxs-lookup"><span data-stu-id="1d59a-158">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="1d59a-159">Para importar a chave pública Diffie-Hellman para o CSP, chame a função [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , passando um ponteiro para o blob de chave pública no parâmetro *pbData* , o comprimento do blob no parâmetro *dwDataLen* e o identificador para a chave Diffie-Hellman no parâmetro *hPubKey* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-159">To import the Diffie-Hellman public key into the CSP, call the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function, passing a pointer to the public key BLOB in the *pbData* parameter, the length of the BLOB in the *dwDataLen* parameter, and the handle to the Diffie-Hellman key in the *hPubKey* parameter.</span></span> <span data-ttu-id="1d59a-160">Isso faz com que o cálculo, (Y ^ X) mod P, seja executado, criando assim a chave secreta compartilhada e concluindo a [*troca de chaves*](../secgloss/e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1d59a-160">This causes the calculation, (Y^X) mod P, to be performed, thus creating the shared, secret key and completing the [*key exchange*](../secgloss/e-gly.md).</span></span> <span data-ttu-id="1d59a-161">Essa chamada de função retorna um identificador para a nova chave de sessão secreta, no parâmetro *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-161">This function call returns a handle to the new, secret, session key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="1d59a-162">Neste ponto, o Diffie-Hellman importado é do tipo **CALG \_ AGREEDKEY \_ any**.</span><span class="sxs-lookup"><span data-stu-id="1d59a-162">At this point, the imported Diffie-Hellman is of type **CALG\_AGREEDKEY\_ANY**.</span></span> <span data-ttu-id="1d59a-163">Antes que a chave possa ser usada, ela deve ser convertida em um tipo de chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="1d59a-163">Before the key can be used, it must be converted into a session key type.</span></span> <span data-ttu-id="1d59a-164">Isso é feito chamando a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) com *DwParam* definido como **KP \_ ALGID** e com *pbData* definido como um ponteiro para um valor [**de \_ ID alg**](alg-id.md) que representa uma chave de sessão, como **CALG \_ RC4**.</span><span class="sxs-lookup"><span data-stu-id="1d59a-164">This is accomplished by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function with *dwParam* set to **KP\_ALGID** and with *pbData* set to a pointer to a [**ALG\_ID**](alg-id.md) value that represents a session key, such as **CALG\_RC4**.</span></span> <span data-ttu-id="1d59a-165">A chave deve ser convertida antes de usar a chave compartilhada na função [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) ou [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="1d59a-165">The key must be converted before using the shared key in the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) or [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span> <span data-ttu-id="1d59a-166">As chamadas feitas para uma dessas funções antes da conversão do tipo de chave falharão.</span><span class="sxs-lookup"><span data-stu-id="1d59a-166">Calls made to either of these functions prior to converting the key type will fail.</span></span>
5.  <span data-ttu-id="1d59a-167">A chave de sessão secreta agora está pronta para ser usada para criptografia ou descriptografia.</span><span class="sxs-lookup"><span data-stu-id="1d59a-167">The secret session key is now ready to be used for encryption or decryption.</span></span>
6.  <span data-ttu-id="1d59a-168">Quando a chave não for mais necessária, destrua o identificador de chave chamando a função [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="1d59a-168">When the key is no longer needed, destroy the key handle by calling the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

## <a name="exporting-a-diffie-hellman-private-key"></a><span data-ttu-id="1d59a-169">Exportando uma chave privada de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="1d59a-169">Exporting a Diffie-Hellman Private Key</span></span>

<span data-ttu-id="1d59a-170">Para exportar uma chave privada Diffie-Hellman, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="1d59a-170">To export a Diffie-Hellman private key, perform the following steps:</span></span>

1.  <span data-ttu-id="1d59a-171">Chame a função [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obter um identificador para o provedor criptográfico do Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="1d59a-171">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="1d59a-172">Crie uma chave de Diffie-Hellman chamando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para criar uma nova chave ou chamando a função [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) para recuperar uma chave existente.</span><span class="sxs-lookup"><span data-stu-id="1d59a-172">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="1d59a-173">Crie um Diffie-Hellman [*blob de chave privada*](../secgloss/p-gly.md) chamando a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , passando **PRIVATEKEYBLOB** no parâmetro *dwBlobType* e o identificador para a chave Diffie-Hellman no parâmetro *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="1d59a-173">Create a Diffie-Hellman [*private key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PRIVATEKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="1d59a-174">Quando o identificador de chave não for mais necessário, chame a função [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) para destruir o identificador de chave.</span><span class="sxs-lookup"><span data-stu-id="1d59a-174">When the key handle is no longer needed, call the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function to destroy the key handle.</span></span>

## <a name="example-code"></a><span data-ttu-id="1d59a-175">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="1d59a-175">Example Code</span></span>

<span data-ttu-id="1d59a-176">O exemplo a seguir mostra como criar, exportar, importar e usar uma chave de Diffie-Hellman para executar uma troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="1d59a-176">The following example shows how to create, export, import, and use a Diffie-Hellman key to perform a key exchange.</span></span>


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
